# Prompts

The prompts I used to build the Study&Go Compass with Claude. This is a selection, in the order I wrote them, copied as typed.

1. [The first brief](#1-the-first-brief)
2. [Checklists: priority, sub-steps, drag to reorder](#2-checklists-priority-sub-steps-drag-to-reorder)
3. [Free-rolling globe and the liquid-chrome look](#3-free-rolling-globe-and-the-liquid-chrome-look)
4. [Still background, gold cells, free roll with auto-turn](#4-still-background-gold-cells-free-roll-with-auto-turn)
5. [Turn it into an app](#5-turn-it-into-an-app)
6. [Tags that pulse on the globe](#6-tags-that-pulse-on-the-globe)
7. [Give a goal to Claude Code, with the mascot](#7-give-a-goal-to-claude-code-with-the-mascot)
8. [Mascot animations](#8-mascot-animations)
9. [Tags in the list, wider panels, progress fill, a sound](#9-tags-in-the-list-wider-panels-progress-fill-a-sound)
10. [Two bug reports](#10-two-bug-reports)

## 1. The first brief

25-11-2026, 01:36

> Build me a desktop web app (single HTML artifact, self-contained, no external libraries) called "Study&Go Compass" — a goal/todo tracker for my startup Study&Go. I will install it as a desktop app, so it must look and feel like a polished native app at \~1440x900.
>
> LAYOUT — three columns, modeled on a skill-logbook app:
> - Left sidebar (\~260px): list of goal categories with name and progress (e.g. "3/6"), a thin progress underline per category, and an overall counter at the bottom like "13 of 19 done" with a progress bar.
> - Center stage (the hero): the Study&Go globe, large and centered.
> - Right panel (\~300px): detail view of the selected todo — title, category, a checklist of subtasks with checkboxes, optional notes, a status chip ("Open" / "In progress" / "Done"), and a primary button "Mark complete".
> - Top bar: app title "Study&Go", a Map/List view toggle, a category filter dropdown, and a search field.
>
> THE GLOBE — the core of the app:
> - Draw the Study&Go logo from scratch as inline SVG: a wireframe globe made of a circular outline plus curved longitude and latitude lines (think a classic globe grid icon, slightly tilted/perspective style), stroke-only, thick rounded strokes.
> - Brand colors: baby light blue (#AECBEA) strokes on a deep navy (#0E2A47) background panel, with a cream/white app chrome around it. Keep it clean and modern.
> - CRITICAL: each enclosed cell between the grid lines of the globe is its own interactive panel (an SVG path with its own fill). Generate the globe so cells are explicit closed paths, not just overlapping lines. Aim for roughly 16–24 usable cells.
> - Each cell represents one todo/goal: filled light blue when done, pale/outlined when open, with a tiny icon or 2–3 letter label inside the larger cells.
> - Hover: the hovered cell smoothly scales up (\~1.15x from its own center, transform-origin on the cell), lifts above its neighbors (raise it in the SVG stacking order on hover), gets a subtle glow/shadow, and shows a tooltip with the todo title. Transitions must be smooth (CSS transitions, \~150ms).
> - Click: the cell gets a selected state (brighter fill + pulsing dashed ring, like a "current" marker), the matching todo highlights in the LEFT sidebar (scroll into view + highlighted background on its row), and the RIGHT panel loads that todo's details. Clicking a sidebar row must also select the matching globe cell — two-way linking.
>
> DATA & BEHAVIOR:
> - Everything persists in localStorage. Seed it with sample Study&Go goals so it looks alive on first open — categories like: Architecture rebuild, Website rebuild, Company setup (SRL), Product, Admin. 15–20 todos total, each with 2–5 checklist subtasks, some done, some in progress.
> - Full CRUD: add a todo (assigns it to the next free globe cell), edit title/category/subtasks, mark complete (cell fills in with a short satisfying animation), delete with an inline confirm (no browser confirm() dialogs anywhere).
> - Checking off all subtasks suggests marking the todo complete.
> - List view toggle: swaps the globe for a simple table of all todos; selection state stays in sync.
> - All dates shown anywhere use DD-MM-YYYY format (day first, never month first).
>
> POLISH:
> - Cream/off-white app background (#FAF6EF-style), soft rounded corners, subtle borders, the navy globe panel as the visual anchor. Typography: a clean sans-serif, generous spacing, nothing cramped.
> - A small footer status line like "18 goals · 7 done · 2 in progress".
> - Keyboard: arrow keys move selection between cells, Enter opens detail, Esc deselects.
> - No alerts, no external network calls, works fully offline

## 2. Checklists: priority, sub-steps, drag to reorder

25-11-2026, 03:00

> it came out a bit broken, (logo) fix that.  
> Regarding the checklists, I'd like them to put them based on priority, based on color, the higher on top the checklist the most important it is, also, I'd like to give the checklist's to-do's a sub todo, in case sometimes certain things have like a step one, step two, and so on..  so give those sub steps numbers within the checklist.  make sure those substeps can be folded down. One more thing regarding the checklist, i want to be able to drag them up or down, if there is one on the buttom, and its more important, i'd like to be able to drag it all the way upwards with it's substeps.

*Sent with 2 pictures attached. The pictures are not in this repo.*

## 3. Free-rolling globe and the liquid-chrome look

25-11-2026, 03:24

> alr now make it that i can turn it also freely, up down vertical left right and so on, but it would always come back to it "default" pose and simply auto-rotate -> and Study&Go Blue deffently wins the look!  I also added in the vault -> in Entry the picture of "flowing-chrome-abstract-blue-style" since i'd like to update the whole compass style acordingly since now if we would add this awsome globe to the mix it would feel out of touch, and we don't want that, we want everything to feel together.  to have a more Abstract liquid-chrome render: flowing polished metal in cool steel blues with warm golden highlights, stretched into smooth motion-blurred streaks that converge toward a central vortex point. Glossy, reflective, almost fluid — the look of blown-up macro chrome or a 3D "liquid metal" wallpaper, with a faint fine-mesh texture in the surface. Clean, modern, tech-ambient feel to the full compase.

## 4. Still background, gold cells, free roll with auto-turn

25-11-2026, 03:49

> i like most things, i simply say what i don't like, i don't like background behind the globe, i was more expexing youd use certain colors, and textures (see images) to update the things round the globe such as, footer, header, side bars, and so on, peferable using the second image i gave you or last one as the background (static) and not moving since the globe is already moving. Also i'd like to have the option if i click on an empty cell, (its selected) and i click again on the same cell (nothing is selected, so the right side bar is empty instead saying "no goals here yet, free cell".
>
> and when its marked to turn it gold, so more gold cold cells would appears over time.
>
> Also regarding the movement of the globe, i don't like it always goes into the default state, lets skip that and let it grab it and role it until it stops by it self, (also i really like the way it would auto-turn by itself) lets bring that back. but if the globe it turned upside down it should simply continueing turning like that in autoturn. (autoturn should be defaulted option).

*Sent with 5 pictures attached. The pictures are not in this repo.*

## 5. Turn it into an app

25-11-2026, 03:55

> perfect its done, now turn it into a app:  
> https://claude.com/resources/articles/install-as-app

## 6. Tags that pulse on the globe

25-11-2026, 04:58

> i want to add like a Tag "#Most important" -> effect: glowing and pulsating red on that cell.  
> Other tag should be "#Due Soon" -> effect: a lighter glowing and pulsating light red effect, slower pulse compared to "Most important".  
> Other tag should be "#Give2Claude" -> effect: glowing and pulsating orange, slower pulse then "Most important".
>
> Update the file, do i need to redownload the app? or does it automatically update it?

## 7. Give a goal to Claude Code, with the mascot

25-11-2026, 13:38

> How do i actually give it to Claude? To finish that one specific task? Ofc giving with the full globe context to Claude Code but having only that specific goal focused. 
>
> The Claude Code Mascot (Clawd) (orange) should be in bottom right side panel where he would ocasionally have small animaitions as jumping and when hover over the mascot (or clicked) asking "Give this goal to Claude Code?" this should be like a talk bubble

## 8. Mascot animations

25-11-2026, 14:09

> Dope! Now add the "take out the laptop and starts to write on it" animation only when clicked on "Yes, copy the brief" its changing animations. Also add the football animation as a random animation that comes up, and also I also like the sleeping animation, make it sleep sometimes at random

*Sent with 1 picture attached. The pictures are not in this repo.*

## 9. Tags in the list, wider panels, progress fill, a sound

25-11-2026, 14:34

> the list area doesn't hold the tags, please fix that. Also, I'd like to sometimes expand my side panels to take them and make them bit bigger, but by default should always it normal size side panel. 
>
> One thing I'd like to add from the design of the 3D logo into the Compass rn is whenver you are in progress with a task, it slowly filles up as "Study&Go blue  solid" and once every task is done and mark complete it should be turning gold (when it marked complete it should have lil dopamine effect as a sound).

## 10. Two bug reports

25-11-2026, 16:31

> one thing i noticed, when dragging my tasks up or down wards, its not that smooth. lets fix that  
> one other bug i noticed is i can't use the lowest cells on the globe to add goals to it.
