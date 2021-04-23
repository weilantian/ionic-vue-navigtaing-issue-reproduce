

A experiment repo that reproduce the navigation animation issue in Ionic Vue while using iOS theme.

Here is the repo I created by using the command

```
ionic start navigatingIssue tabs
```


After that, I configured the app in main.ts to use only iOS theme in order to reproduce this bug in the Chrome on my Mac.

```
const app = createApp(App)
  .use(IonicVue,{
    mode: 'ios'
  })
  .use(router);
```

And I created two blanks pages with `<ion-page>`tag, and I have configured the router to point one page to `/page1`, another to `/page2`

After that, I created a button which uses `@click` to triggers the `router.push()` 

Here is a digram explaning the way this bug might be triggered

![Untitled Diagram 2](https://user-images.githubusercontent.com/13176782/115822065-7ef35e80-a436-11eb-879f-248fa2e70650.png)


A record creared by using a Mac screen recorder which shows how to repoduce the bug:

https://user-images.githubusercontent.com/13176782/115821285-1c4d9300-a435-11eb-8c7c-be06e9b1ecba.mp4

I presonally believe this bug is a issue with the intergration of vue router.
