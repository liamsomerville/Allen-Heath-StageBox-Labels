
What it is: a single-file, offline HTML patch sheet generator for Allen & Heath I/O. You pick a rack or stage box, it draws the rear panel, and you type a label under every socket.

#Supported hardware
- dLive MixRacks: DM64, DM48, DM32, CDM64, CDM48, CDM32
- Stage boxes / AudioRacks:
     - GX4816,
     - DX168,
     - AR2412,
     - AB168
- Expanders:
- DM/CDM/GX4816 can add up to 2× DX168. The second is only enabled once the first is ticked.
- AR2412 can add 1× AB168.
- DX168 and AB168 have no expander options.

# Panel drawing (SVG)
- Female XLRs for inputs and male XLRs for outputs, numbered and laid out in that unit’s column and row grid.
- An editable label box under every socket. Labels print in uppercase monospace.
- Bottom strip shows:
- IEC inlet and power switch, plus a second PSU inlet on DM racks
- Model wordmark
- Network ports (gigaACE/DX/Net, GX/Link, dSNAKE/MON/EXP)
- Earth terminal
- Expander panels stack below the main unit, scaled proportionally to the widest panel.

# Title block
- Logo upload, embedded as base64 and removable
- Show/Event, Engineer, Date and Doc Version fields

# Persistence and I/O
Autosaves to localStorage on every keystroke, including device, expanders, labels, title block and logo.
Save file / Load file exports and imports the full state as JSON, named after the show.
Clear wipes socket labels only and keeps the device, title block and logo.

# Output
- Print layout is A4 landscape with 8 mm margins.
- The toolbar and controls are hidden when printing, and panels and the title block are kept from splitting across pages.
