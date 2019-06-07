## AWS Community Day hugo theme

This theme is intended for the AWS Community to use and build upon when hosting [AWS community days](https://aws.amazon.com/events/community-day/)

### Requirements

- [hugo](https://gohugo.io)

### Set up base site

Run the follow commands in your terminal:

```bash
hugo new site MY_CITY_community_day
cd MY_CITY_community_day
git init
```

### Add the theme

Now lets import the theme:

```bash
git submodule add https://gitlab.com/ric_harvey/aws-community-day-theme.git themes/aws-community-day-theme
```

This imports the theme into __themes/aws-community-day-theme__

### Enable the theme on your site

Run the following commands to get started:

```bash
cd themes/aws-community-day-theme/exampleSite
cp -Rf * ../../../
rm config.toml
```

To change the name of the event edit __config.yaml__ The agenda details are set within this file also. Add static files to the static folder and if you want to tweak the theme copy __themes/aws-community-day-theme/layouts/FILE_TO_TWEAK__ to __layouts/FILE_TO_TWEAK__ in the root directory. The same methof of copying out of the theme to your root should be done for static content also CSS, JS, etc..

### Testing it all out

To test your site:

```bash
hugo server --watch
```

Now browse to [http://localhost:1313](http://localhost:1313)

**Note:** Before you go live edit config.yaml and change the base URL
