This little drupal module facilitates conversion of Drupal 6 style user profile fields to Drupal 7 user entity fields. This one is rough one time convertor, no effort was spent on UI or extensive in-module error handling.

**Always make a database backup first.** You may really need it.

Enable as any other module. It will read your current D6 style profile fields and create matching user entity fields. Then navigate to Configure -> People -> Migrate Core Profile to User Entity and start conversion process.


*Limitations:*

1. Original D6 profile machine field name has to be shorter than 25 characters. So newly created d7 user entity field would be less than 32 characters with added 'field_' prefix.


You'll want to rearrange your converted fields or change type of select element at Configure -> People -> Account settings -> Manage fields.

If everything looks good, you may be safe to disable 'profile' module and delete 'profile*' fields from db.

This version can handle link and checkbox fields. And has this readme. Big thanks to @markwkoester for original version.
