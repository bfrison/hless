# Presentation
`hless` uses `highlight` and `less` to allow you to see a script in a pager, with syntax highlighting.  
`hless` is a Python script which pipes the content of your file into `highlight` and then `less`.
# Installation
`hless` is for now only supported on Debian distributions on Linux. To install execute
```bash
sudo apt install python3.10
sudo apt install highlight
```
# Instructions
In the console, execute
```bash
hless <file_names>
```
to open the desired files in `hless`. If there are more than one file, they can be listed with white space between them. In `hless`, you can navigate between multiple files using normal `less` commands (:p and :n, or you can type h to see the help page).  
`hless` will decide which language's syntax to apply based on the file extension. To override the file extension, use -S argument before the file names to manually enter the desired language. E.g.
```bash
hless -S bash script_name
```
to see the content of `script_name` in `bash`.
You can pipe the output of a process into `hless` by leaving the `<file_names>` part empty or using a hyphen. When piping, you must specify the syntax manually using -S.
