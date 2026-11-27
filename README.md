# Study&Go Compass

A goal tracker built around the Study&Go globe logo. Each cell on the globe holds one goal. The whole app is one HTML file.

Check it out: https://claude.ai/artifact/XVDvZnh6uE689MTBPf9MYo

## How it works

<table>
<tr>
<td width="260" valign="top">
<img src="globe%20logo%20gif%20V1.gif" width="220" alt="Study&Go globe animation">
</td>
<td valign="top">


#### The Compass with goals placed on the globe
The globe has 60 cells. Click an empty cell to put a goal there, then give it a title, a category you type yourself, a due date and a checklist.

Drag the globe to roll it in any direction. Left alone, it keeps turning on its own.

</td>
</tr>
<tr>
<td width="260" valign="top">
<img src="Creating_new_goal_gif.gif" width="220" alt="Creating a new goal">
</td>
<td valign="top">

#### A cell changes as the goal moves along:

An open goal is a plain chrome cell.
A goal in progress fills with solid Study&Go blue as its checklist gets ticked.
A completed goal turns gold, and the app plays a short chime.

</td>
</tr>
<tr>
<td width="260" valign="top">
<img src="Give_goal_to_Claude_gif.gif" width="220" alt="Creating a new goal">
</td>
<td valign="top">

####  Feeling lazy? Give your task to Claude Code! 

Create your Goal, and copy & past it, into Claude Code within the application it self! It will copy your goal as your primary task and keep all the rest of your globe as background. 

</td>
</tr>
<tr>
<td width="260" valign="top">
<img src="Checklist_review_gif.gif" width="220" alt="Creating a new goal">
</td>
<td valign="top">

#### Checklists

The order of a checklist is its priority. The item at the top matters most and the colour follows the position. Drag an item up or down to change its priority, and its sub-steps move with it. Sub-steps are numbered and fold away.

</td>
</tr>
<tr>
<td width="260" valign="top">
<img src="Tag_review_gif.gif" width="220" alt="Creating a new goal">
</td>
<td valign="top">

#### Tags

A goal can carry three tags, and each one makes its cell pulse on the globe:

Tag	Effect on the cell
#Most important	a red line inside the cell that beats like a heart
#Due Soon	a light red line that breathes slowly
#Give2Claude	an orange line that breathes slowly

The List view shows the same goals as a table, with their tags.

</td>
</tr>
</table>



## New in this version

- **Priority list.** Open goals are ranked in the left panel. Drag the number to move a goal up or down. The globe shows your number 1 and its first open step under "Next up".
- **Finished goals become a spiral.** Every finished goal turns into a gold ball on a spiral that climbs and turns slowly. Click a ball to open that goal.
- **A universe of globes.** Once a globe is 60% done, "Create new globe" appears in the left panel. Your other globes float in the background. Scroll out past the smallest zoom to bring them forward, then click one to go there.
- **Your own zoom.** Ctrl + and Ctrl - resize the app and it remembers the size. Scroll over the globe to zoom it.
- **Neon and Shine.** Neon draws a light along every cell edge. Shine adds a glass rim and a soft halo. Both have a switch next to Auto-turn.
- **Calmer chrome.** A goal in progress fills up inside its cell's frame. The selected goal turns blue-white on the globe and in the spiral. The globe never ends up upside down.
- **Preview a full globe.** This link under Overall shows what a finished globe looks like without saving anything.

## Final result:
<img src="App_review_V6_gif.gif" width="1000" alt="how it looks">



## Prompts

The prompts used to build the Compass are in [PROMPTS.md](PROMPTS.md), in the order they were written.
