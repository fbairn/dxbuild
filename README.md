This builds a simple dyno that can run Salesforce DX commands.

##Create a new app with buildpack
heroku create myapp --buildpack https://github.com/fbairn/dxbuild.git

##Using with an exsisting dyno

Set the default buildback
heroku buildpacks:set https://github.com/fbairn/dxbuild.git -a Appname

This sets the first buildback to Node.
heroku buildpacks:add --index 1 heroku/nodejs -a Appname