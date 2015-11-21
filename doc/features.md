
Features
===============================================================================


Project Discovery
-------------------------------------------------------------------------------

Ember.js projects are automatically discovered when imported via 
`File → New → Project from Existing Sources...`. The importer will look for an
`app/app.js` file and will flag the project as an Ember.js project if the file
exists.

The language level for Ember.js projects is automatically set to ES6 and
JSHint support is enabled using the `.jshintrc` file.


Marking special folders
-------------------------------------------------------------------------------

The importer will mark certain folders like this:

- `app` as `Sources Root`
- `public` as `Resources Root`
- `tests`, `tests/unit` and `tests/integration` as `Tests Root`
- `dist` and `tmp` as `Excluded`

![Project View](project-view.png)

This will cause the "Packages" view to look like this:

![Packages View](packages-view.png)


Quick Navigation
-------------------------------------------------------------------------------

### `Navigate → Class...`

The plugin is indexing all typical components in the `app` folder and is
providing them for quick access via the `Navigate → Class...` action. Currently
supported are:

- Adapters 
- Components
- Controllers
- Helpers
- Models
- Routes
- Serializers
- Services
- Transforms

The indexer will transform file paths into class names by capitalizing the
path parts and appending a type suffix

Example: `app/routes/pets/index.js` will be indexed as `PetsIndexRoute`

  ![Navigate → Class...](goto-class.png)


### `Navigate → Related Symbol...`

The plugin provides an implementation for the `Navigate → Related Symbol...`
quick navigation.

Example: Invoking the action inside of `/app/routes/crate/index.js` will
switch to the `/app/controllers/crate/index.js` file if it exists.
 
The following groups of files can be cycled like this:
 
- `controllers`, `routes`, `templates`
- `components`, `templates`
- `adapters`, `models`, `serializers`


-------------------------------------------------------------------------------

Most screenshots in this document are taking from an import of the 
[crates.io](https://github.com/rust-lang/crates.io) project.