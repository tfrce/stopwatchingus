stopwatchingus
==============

## Development

Learn Jekyll

```
jekyll serve --watch
```



## Deployment

We deploy via pushing to a git repository on the production server. To add the remote origin

__make sure to use the correct username (e.g. jduncks, sina, thomas)__

```
git remote add production thomas@2.stopwatching.us:/home/rritf/repos/stopwatching.us.git
```

Once the production server receives this, it runs `jekyll build`

To push to the production server simply

```
git push production gh-pages
```
