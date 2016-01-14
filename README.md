# Roobiedocks-Adventure
First Ruby challenge at Udacity
# Roobiedocks & Reflect
# ~~~~~~~~~~~~~~~~~~~~~

# You wake up, only to find yourself in an unfamiliar land...

# You wander in the wilderness and come across a door.
# All it says is "Welcome to Roobiedocks".
# You try opening it, but it is locked.

# Below the lock is a code along with a series of instructions.
# Follow these instructions, it looks like that will unlock the door.

code = "M.E?CIQN E?RS, D?NA EQC,IN S,,I Z?TQAM,"

# ---------------------------------------------------------------
# | 0. Remove the first character in the code.                  |
# | 1. Insert the string "A EW? O" at the code's 11th position. |
# | 2. Remove all instances of the characters 'Q', '?', and ','.|
# | 3. STOP SHOUTING. Make the entire code lowercase, for now.  |
# | 4. Reverse the order of the characters in the code.         |
# | 5. Capitalize the first letter of the code.                 |
# | 6. `puts` the code to reveal the message.                   |
# ---------------------------------------------------------------

# All your code should go between these lines!
# ========================
"M.E?CIQN E?RS, D?NA EQC,IN S,,I Z?TQAM,".gsub(/^./, "")
=> ".E?CIQN E?RS, D?NA EQC,IN S,,I Z?TQAM,"

".E?CIQN E?RS, D?NA EQC,IN S,,I Z?TQAM,".insert(11, 'A EW? O')
=> ".E?CIQN E?RA EW? OS, D?NA EQC,IN S,,I Z?TQAM,"

code=".E?CIQN E?RA EW? OS, D?NA EQC,IN S,,I Z?TQAM,"
code.delete! 'Q'
=> ".E?CIN E?RA EW? OS, D?NA EC,IN S,,I Z?TAM,"

code = ".E?CIN E?RA EW? OS, D?NA EC,IN S,,I Z?TAM,"
code.delete! '?'
=> ".ECIN ERA EW OS, DNA EC,IN S,,I ZTAM,"

code = ".ECIN ERA EW OS, DNA EC,IN S,,I ZTAM,"
code.delete! ','
=> ".ECIN ERA EW OS DNA ECIN SI ZTAM"

".ECIN ERA EW OS DNA ECIN SI ZTQAM".downcase
=> ".ecin era ew os dna ecin si ztam"

".ecin era ew os dna ecin si ztam".reverse
=> "matz is nice and so we are nice."

"matz is nice and so we are nice.".capitalize
=> "Matz is nice and so we are nice."

code = "matz is nice and so we are nice."
code[0] = code[0].capitalize
puts code

Matz is nice and so we are nice.
=> nil

# ========================

# What a nice passcode.
