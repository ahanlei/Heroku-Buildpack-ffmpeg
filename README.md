# heroku-buildpack-ffmpeg-latest

Push: [![Test](https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest/workflows/Test/badge.svg?branch=master&event=push)](https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest/actions?query=workflow%3ATest+event%3Apush+branch%3Amaster)  
Scheduled: [![Test](https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest/workflows/Test/badge.svg?branch=master&event=schedule)](https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest/actions?query=workflow%3ATest+event%3Aschedule+branch%3Amaster)


A Heroku buildpack for ffmpeg that always downloads the latest [static build](http://johnvansickle.com/ffmpeg/).
Unlike other build packs, it is  never precompiled.

## Usage
-Run the following from the heroku command line:

```
heroku buildpacks:add --index 1 https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest.git
```

Note: This buildpack should be added before the main language buildpack (by using `--index 1`),
since the application process types are calculated from the last buildpack in the list if no
`Procfile` is specified.

**Thanks To:**
- (johnvansickle.com)[static build](http://johnvansickle.com/ffmpeg/).
