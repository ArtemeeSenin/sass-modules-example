# SASS New Module System Example Of Use

## Importing styles

The `@use` rule is a replacement for old `@import` and every such import is scoped for the file imported it this way. 

To add a shorter name for imported module (by default the filename is used) specify desired name after `@use 'my-lib' as lib` or make it global with asterisk like `@use 'my-lib' as *`. The last syntax is handy for libraries with `@forward` as the global styles will be appled only to library scope and not for the end user.

## Exporting variables, mixins, functions

The `@forward` rule is hadny when creating some libraries to squash all internal files into one for library users. `@forward` can configure variables before export and change visibility of exported members by using `show` and `hide`.
The placeholders `%placeholder` are accessible without explicit show or hide declaration.

## Private members

All entities which names start with `_` or `-` are private to modules they are decalred in.