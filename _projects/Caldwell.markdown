---

layout: project
title: The Case of Caldwell Concoctions
thumbnail: \assets\caldwellThumb.png
videolink: https://www.youtube.com/watch?v=ydXjEKqJtEs
youtubeId: ydXjEKqJtEs
shortdescription: Narrative puzzle game created for Pirate Software Game Jam 15
permalink: /Caldwell
priority: 2
---

PAGE IN PROGRESS
<h1>Summary</h1>
The Case of Caldwell Concoctions is a game I created in 2 weeks as a solo project, as my submission to the Pirate Software Game Jam 15. From a technical standpoint, it is simpler than my other projects and did not involve much complex programming, instead focusing more on story and environmental details. The game did however feature:
- A complete, short story experience with a finished ending.
- 9 levels, each with a puzzle.
- A short cutscene in every level.
- Utilisation of Unity's player prefs system to allow for game progress to be saved between multiple sessions on the web.
- A notebook that will unlock new information as the game progresses.

<h1>Visuals</h1>
The visual style of the game was created with a combination of RenderTextures and post processing.
To achieve the pixelated style, the game first renders the scene to a RenderTexture with a low resolution. This texture is then projected onto another camera, and rendered to the screen. This also means that the UI scales and changes easily as the screen size changes.

The post processing uses SSAO and colour grading to make the colours and the visuals pop more: older games of this style tend to have more saturaded and brighter colours.

<h1>Potions</h1>
The potions in the game were handled using an enum for their names, so that when checking if the combination was correct, no string comparisons were needed. However, this approach ended up being more difficult to handle than string comparisons, as serializing enums can have unintended consequences. For example, if I set the name of a potion in the Unity inspector, but then altered the enum to have new values, the value of the potion in the inspector changed, as internally the enums are just representations of integers. This meant that whenever I added a new potion enum value, it had to be added to the end of the enum, as to not offset any previous values. If I had simply used string comparisons then this would not have occured.

<h1>Player prefs</h1>
used to save the game and such

<h1>What went well</h1>
I was very happy that I managed to get the game fully complete by the deadline of the game jam, which shows that my initial planning and scope for the game was reasonable and appropriate for the timeframe. I received a lot of comments and feedback on the game, a lot of which was positive and praising the aspects I focused on, such as the writing and environmental storytelling.
<h1>What I would improve</h1>
Some feedback on the game indicated that there should be better feedback for when the player gets a potion wrong, which I agree with. I think a little message telling the player that thwy are incorrect would help the clarity of the game a lot. Some more feedback was that the gameplay was a bit simplistic, and to be a full game, new mechanics would have to be added, which I also agree with. The game could potentially have multiple endings depending on the player's actions throughout the game, though this was of course outside the scope of a game jam project.