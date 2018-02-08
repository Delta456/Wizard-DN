Wizard-DN
--------------

This is a day/night system initially designed on Fire Red and soon to be ported to Emerald and (maybe) Ruby. The core principle in this D/N system is gradients and ease of use for the user. Instead of doing sloppy, faster masks, this D/N system uses an intelligent and fast blending system which will blend 32 bit ARGB colors with the existing colors in the palette, allowing for more natural colors depending on the time of day. In addition to the palette blending, a 144 color gradient is used to create a smooth transition between times of day. The difference is clearly visible in these two pre-rendered GIFs which were made using MEH:

![GIF](http://giant.gfycat.com/LateSpiffyHyrax.gif)
![GIF](http://fat.gfycat.com/FlippantBoilingFeline.gif)

Full Source is obviously provided here under GPLv3. This means that any modifications publicly released must also provide their source code as well.


GPL License
---------------

Copyright (C) 2014 Shiny Quagsire, diegoisawesome, and others

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>
To contact the author of this work, e-mail him at mtinc2@gmail.com


**THIS FORK WORKS WITH NAVENATOX'S PALLETE PATCH**
1. Apply the Pallete Patch or compile it from the repo. 
2. Insert `Navenatox_Pallete_Patch_Fix.asm`.
3. Insert `RTC.asm`

In Line 436 `updateNPCPal: ......... .word 0x08XXXXXX+1`.  with XXXXXX being the offset of where you just inserted the `Navenatox_Pallete_Patch_Fix.asm`. This is not a pointer, do not reverse or add anything to the offset, just change the number after 0x08 exactly where you inserted it and keep the +1 after it.


If I have put it in 9045F0, I will write `0x089054F1`.

4. Put all the other asm files.

