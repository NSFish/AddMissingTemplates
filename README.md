将OC category等模板加入到Xcode 6中，用的时候请注意根据Xcode版本修改一下路径中Xcode的命名。
Add OC category templates to Xcode 6，pls modify PROJECT_TEMPLATES_PATH and FILE_TEMPLATES_PATH as your need.

# !/bin/sh

SAVEIFS=$IFS
IFS=$(echo -en "\n\b")

PROJECT_TEMPLATES_PATH="/Applications/Xcode6-Beta3.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/Project Templates/iOS/Application"
FILE_TEMPLATES_PATH="/Applications/Xcode6-Beta3.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/File Templates/Source"

EMPTY_APPLICATION_PATH="$PWD/Empty Application.xctemplate"

OC_CATEGORY_PATH="$PWD/Objective-C category.xctemplate"
OC_PROTOCOL_PATH="$PWD/Objective-C protocol.xctemplate"
OC_EXTENSION_PATH="$PWD/Objective-C class extension.xctemplate"

cp -R $EMPTY_APPLICATION_PATH $PROJECT_TEMPLATES_PATH

cp -R $OC_CATEGORY_PATH $FILE_TEMPLATES_PATH
cp -R $OC_PROTOCOL_PATH $FILE_TEMPLATES_PATH
cp -R $OC_EXTENSION_PATH $FILE_TEMPLATES_PATH

IFS=$SAVEIFS
