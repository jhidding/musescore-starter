# musescore-starter

Start script and desktop files for MuseScore Studio AppImages

## Why

When you download a [MuseScore Studio AppImage](https://musescore.org/nl/download), you have to make sure that this image is made executable with `chmod +x` and then you can run MuseScore from the command line. When MuseScore installs an update, the new image is placed in the same directory as the old one.

Many Linux distributions ship some version of MuseScore, but when you encounter problems the maintainers only accept those that are reproducible from official AppImages.

Using the files in this repository you can run MuseScore from your desktop, and the Bash script automatically selects the latest image to run with.

## How

This package is (non-)designed for use with the `stow` package manager on Linux to manage applications in `~/.local` directory. That means that you clone this repo into `~/.local/pkg/musescore`, then run `stow musescore` from the `~/.local/pkg` directory.

Make sure that `~/.local/pkg/.stow-global-ignore` contains the following:

```
.gitignore
README.md
LICENSE
```

That way, these files (and any like them in other stow packages) are not linked down to `~/.local`.

## License

The little content in this package is distributed under the GPL 3.0, to match the license under which MuseScore itself is distributed. The MuseScore Studio icon was unceremoniously ripped from the [musescore.org](https://musescore.org) website.

> MuseScore-starter
> Copyright (C) 2025  Johan Hidding
> 
> This program is free software: you can redistribute it and/or modify
> it under the terms of the GNU General Public License as published by
> the Free Software Foundation, either version 3 of the License, or
> (at your option) any later version.
> 
> This program is distributed in the hope that it will be useful,
> but WITHOUT ANY WARRANTY; without even the implied warranty of
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
> GNU General Public License for more details.
> 
> You should have received a copy of the GNU General Public License
> along with this program.  If not, see <http://www.gnu.org/licenses/>.

