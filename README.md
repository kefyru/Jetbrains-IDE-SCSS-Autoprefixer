# Jetbrains-IDE-SCSS-Autoprefixer
SCSS (SASS) Compile and PostCSS Autoprefixer for Jetbrains IDE (Rider, Webstorm, PHPStorm) 

1. Install sass, postcss, autoprefixer:
```
npm install -g sass postcss autoprefixer
```
2. Go to `Preferences` -> `Tools` -> `File watchers`
3. Add SCSS wathcer:<br/>
Program: `sass`<br/>
Arguments: `$FileName$:$FileNameWithoutExtension$.css`<br/>
Output aths to refresh: `$FileNameWithoutExtension$.css:$FileNameWithoutExtension$.css.map`
<img width="746" alt="2" src="2.png">
4. Add another SCSS watcher (to the end):<br/>
Program: `postcss`<br\>
Arguments: `$FileNameWithoutExtension$.css --replace --use autoprefixer`<br/>
Output paths to refresh: `$FileNameWithoutExtension$.css`<br/>
<img width="746" alt="3" src="3.png">
Check order:
<img width="746" alt="1" src="1.png">
