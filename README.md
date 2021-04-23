

A experiment repo that reproduce the navigation animation issue in Ionic Vue while using iOS theme.

Here is the repo I created by using the command

```
ionic start navigatingIssue tabs
```

And I created two blanks pages with `<ion-page>`tag, and I have configured the router to point one page to `/page1`, another to `/page2`

After that, I created a button which uses `@click` to triggers the `router.push()` 

Here is a digram explaning the way this bug might be triggered

![Untitled Diagram 2](https://user-images.githubusercontent.com/13176782/115821235-063fd280-a435-11eb-93f6-b354c21331d9.png)

A record creared by using a Mac screen recorder which shows how to repoduce the bug:

https://user-images.githubusercontent.com/13176782/115821285-1c4d9300-a435-11eb-8c7c-be06e9b1ecba.mp4

I presonally believe this bug is a issue with the intergration of vue router.
