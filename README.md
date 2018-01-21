## GunUi elements
GunUi is a set of webcomponents that enables you - the frontend developer - to build complex - Gun - applications without writing any ( well...almost) javascript

Every gunui- element has just 2 required attributes "soul" and "prop" that will link the element to a certain data-point.
## Note:
Although `gunui-base` is the most important peace of the gunui elements, it has no visual appearance by itself.
## Purpose of `gunui-base`
* main element for all 'gunui-' elements.
* Setup Gun by just providing attributes
* makes sure that every gunui- element has the required properties and methods.
* Creates global nameSpace 'GunUi' where 'GunUi.gun' will be the global Gun instance
* ...and then some...we'll get to that when using the elements

#### Without `gunui-base` none of the gunui elements will work!

#### You should use this only once in your main document!

## But Why?
If you don't fully understand the purpose of gunui take a look at some of the actual gunui- elements. ( Not yet there though :) )

## (NPM) Install Gun
'Gun' is not provided as bower module so we'll have to use NPM.

```
npm install gun
```
## (Bower) Install gunui
( When Polymer 3 arrives we can skip the bower part, but for now...)
```
bower install gunui-base --save
```
## Your main document
```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, minimum-scale=1, initial-scale=1, user-scalable=yes">
    <title>todo</title>
    <meta name="description" content="description">
    <script src="/bower_components/webcomponentsjs/webcomponents-loader.js"></script>

    <!-- import gunui-base -->
    <link rel="import" href="/bower_components/gunui-base/gunui-base.html">
  </head>
  <body>
    <--
      Place `gunui-base` in your body
      set peers as comma seperated string ( mind the quotes!!)
      DO NOT INITIATE GUN YOURSELF ( don't do `var gun = Gun()`)
    -->
    <gunui-base peers="'http://localhost:8081/gun','http://my-gun-server/gun'" '></gunui-base>
  </body>
</html>
```
That's it.

<b>NOTE:<br>
Gun is available as 'GunUi.gun'</b>

## Now what?
Now you are ready to start building great apps with Gun but without having to write javascript :). Take a look at the GunUi elements available.
