---
title: Sqeleton
---
Sqeleton is a Qt project template to start a new project with a ready structure.

## File structure

- `.gitignore`: usual files that git should ignore in the project
- `.clang-format` and `.editorconfig`:
  these files are used to maintain a uniform
  code style. It mostly depends on programming habits and so it can be modified
  to suit your needs (same for all other files),
  but I'm curious to see if a common preference could be possible to be set.
- `cmake`: contains the support files for the resources
  and should not be modified per project (Pull Requests are welcome).
- `Config.cmake`: Project specific CMake configuration file, which must be modified.
- `src`: the usual source directory.
- `external`:
  contains git submodules required for the project, currently only a fork
  of LXQt build tools because some required changes.
- `resources`:
  icon, about dialog content - generic appdata/metainfo and desktop file templates.

## Usage

- From the [Github project page], when creating a new project based on Sqeleton,
  click the green `Use this template` dropdown button and select
  `Create a new repository` instead of fork, see the related [documentation] page
  for further information.
- Set the project name in `CMakeLists.txt` and edit `Config.cmake`.
- Replace `resources/icons/application.icon` with the appropriated icon for
  the new application without changing the file name.
  If not a `svg`, edit `PROJECT_ICON_FORMAT` in the configuration file: the name
  of the resulting icon will be set automatically during the CMake configuration.
- If the translations directory will be moved in a different position,
  set the new path in `PROJECT_TRANSLATIONS_DIR` in the configuration file.
- Adapt the resource file in `resources/resources.qrc` if needed.


[Github project page]: https://github.com/qtilities/sqeleton/
[documentation]: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template
