# DX Build

This builds a simple Heroku dyno that can run Salesforce DX commands.

## Create a new app with buildpack

heroku create myapp --buildpack https://github.com/fbairn/dxbuild.git

## Using with an exsisting dyno

Set the default buildback

heroku buildpacks:set https://github.com/fbairn/dxbuild.git -a Appname

## Set the Node buildpack

This sets the first buildback to Node.

This needs to be done for both creating a new dyno and adding to an exsisting one.

The node buildpack must come first.

heroku buildpacks:add --index 1 heroku/nodejs -a Appname
