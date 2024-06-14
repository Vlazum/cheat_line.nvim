# cheat-line.nvim

Cheat line is a very simple vimscript based neovim plugin that helps with navigating within the currently 
selected line.Cheat line consists of two separate lines by default located above the cursor line.They 
point to the beginning of each word within that line using relative numbering.

![Screenshot from 2024-06-01 15-56-11](https://github.com/Vlazum/cheat_line.nvim/assets/121399271/ab674ef0-7e8e-4915-b3c2-d6e789d89a13)


## commands:

`ToggleCheatLine`      - toggles the cheat line

`ChangePointingMode`   - flips the value of `points_to_first_char`

`UpdateCheatLine`      - updates the cheat line

## setup
Cheat line can function properly without setup however some properties can be adjusted.
For changing properties use `cheat_line#config` function. The functoin takes dictionary of properties you would like to change and values that you would like to asign to them. Example: `call cheat_line#config({'points_to_first_char' : 0})`

### adjustable properties:

| Property name          | Description                                                                                                     | Default value |        
| ---------------------- | --------------------------------------------------------------------------------------------------------------- | ------------- |
| `points_to_first_char` | if set to 1 points to the first character in each word of a cursor line. Points to the last character otherwise | 1             |
| `L1_highlight_group`   | defines the highlight group of the first cheat line                                                             | 'Ignore'      |
| `L2_highlight_group`   | defines the highlight group of the second cheat line                                                            | 'Ignore'      |
| `L1_relative_pos`      | defines position of the first line relative to the cursor line                                                  | -1            |
| `L2_relative_pos`      | defines position of the second line relative to the cursor line                                                 | -2            |
| `L1_pos_if_too_high`    | defines position of the first line if it has gone above the line 0                                             | 2             |
| `L2_pos_if_too_high`    | defines position of the second line if it has gone above the line 0                                            | 1             |        
| `L1_pos_if_too_low`     | defines position of the first line if it has gone below the last line in the file                              | -1            |
| `L2_pos_if_too_low`     | defines position of the second line if it has gone below the last line in the file                             | -2            |
> *you can run `:so $VIMRUNTIME/syntax/hitest.vim` command to find more highlight groups*
