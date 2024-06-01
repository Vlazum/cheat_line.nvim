# cheat_line.nvim

Cheat line is a very simple neovim plugin that helps with navigating through line.
Cheat line consists of two separate lines by default located above the cursor line.
They point to the begining of each word within that line using relative numbering.

![Screenshot from 2024-06-01 15-56-11](https://github.com/Vlazum/cheat_line.nvim/assets/121399271/ab674ef0-7e8e-4915-b3c2-d6e789d89a13)


## setup
The cheat line does not require any setup to run properly, however if you would like to you could change some things:
All of the adjustable properties are located in `g:cheat_line_config` dictionary.

### Properties:

`points_to_first_char` - if set to 1 then points to the first character in each word of a cursor line. Points to the last character otherwise (default: 1)

`L1_highlight_group`   - defines the highilight group of the first cheat line (default: 'Ignore')

`L2_highlight_group`   - defines the highilight group of the second cheat line (default: 'Ignore')

`L1_reletive_pos`   - defines positoin of the first line relative to the cursor line (default: -1)

`L2_reletive_pos`   - defines positoin of the second line relative to the cursor line (default: -2)

`L1_pos_if_to_high`   - defines positoin of the first line if it has gone above the line 0 (default: 1)

`L2_pos_if_to_high`   - defines positoin of the second line if it has gone above the line 0 (default: 2)

`L1_pos_if_to_low`   - defines positoin of the first line if it has gone below the last line in the file (default: -1)

`L2_pos_if_to_low`   - defines positoin of the second line if it has gone below the last line in the file (default: -2)

### Functions:

`Toggle_cheat_line()` - toggles the cheat line

`Change_pointing_mode()` - flips the value of `points_to_first_char`
