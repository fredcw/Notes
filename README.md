## Add tile effect to Windows 10 Light theme in cinnamon

For grey tiles open the file `~/.themes/Windows-10/cinnamon/cinnamon.css` and find the line that reads: `border: 2px solid transparent;` (line 1524) and change it to: `border: 2px solid rgba(20, 20, 20, 0.9);`

Then add another line following this one that reads: `background-color: #3f3f3f;`

Also add the line "background-color: #3f3f3f;" at line 1535.

It should end up looking like this:
```
.menu-application-button {
  padding-top: 7px;
  padding-left: px;
  padding-right: 0;
  padding-bottom: 7px;
  max-width: 10px;
  border: 2px solid rgba(20, 20, 20, 0.9);
  background-color: #3f3f3f;
}

.menu-application-button-selected {
  padding-top: 7px;
  padding-left: 7px;
  padding-right: 7px;
  padding-bottom: 7px;
  color: #ffffff;
  border: 2px solid #ffffff;
  background-color: #3f3f3f;
}
```
You can do the same thing with Windows-10-Dark-Master theme which is also in ~/.themes/ but the line numbers are slightly different, eg. 1527 instead of 1524.

If you prefer the blue tiles instead of grey just change the 2 background-color lines to "background-color: #0078d7;" instead. When you make the changes, save the file and restart cinnamon.
