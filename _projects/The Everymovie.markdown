---

layout: project
title: The Everymovie (NUCATS Game Jam 2023)
thumbnail: \assets\everymovie.png
videolink: https://www.youtube.com/watch?v=ctd_rHOdPSU
youtubeId: ctd_rHOdPSU
shortdescription: Minigame-based Game Jam created in 2 weeks in Unity.
permalink: /Everymovie
priority: 4
---

<h1>Play the Game</h1>
<iframe frameborder="0" src="https://itch.io/embed/1981362" width="552" height="167"><a href="https://heavymetalgamedev.itch.io/the-everymovie">The Everymovie by HeavyMetalGameDev</a></iframe>
<h1>Summary</h1>
The Everymovie was my submission into the Newcastle University Computing And Technology Society's 2023 game jam, and it ended up winning the jam. It was technically a team project as I had some help from a friend to create some of the art and animations, but the programming, gameplay and music were all done by me, along with a lot of the art assets. The rules for the jam were:
- The game must run on the web.
- The game must be high score based.
- The game must follow the theme "A day at the movies"

<h1>Game Idea</h1>
When the theme was released, my first thought for how to make a game related to the theme was to involve parody of some kind. The next thought was to parody multiple movies, and taking the high score requirement into account, I decided a minigame-based game would be a fun idea.
<h1>Gameplay</h1>
My main inspiration for the game was the WarioWare franchise, in which many small minigames lasting only a few seconds are played in succession. Gameplay wise, the inspiration is very clear: the player plays a minigame for a few seconds, and if they win they continue, if they fail they lose a life.
A limitation I decided to impose on the game was that to keep the minigames simple and understandable, the only controls for the game would be WASD and Space. Not every minigame had to use both, but limiting myself to these inputs made designing the minigames much easier.

![image](\assets\movieWin.png)
<h6>Winning a minigame gives points and a visual effect where cash is thrown by the audience.</h6> 


<h1>Minigames</h1>
By the end of the jam, I had only managed to create 4 unique minigames, but i was still happy with the end result. The minigames I had were:
- A Lord of the Rings parody, where you mash spacebar to drop an amulet into a pit of lava.
- A Ghostbusters parody, where you aim with WASD and press space to shoot ghouls.
- A Back To The Future parody, where you are in a car and press A or D at the correct time to avoid time paradoxes.
- A Spiderman parody, where you use WASD to avoid bombs being dropped by a villain.

![image](\assets\movieCar.png)
<h6>Back to the Future inspired minigame.</h6> 

![image](\assets\movieSpider.png)
<h6>Spiderman inspired minigame.</h6> 
Overall, I would have liked to add many more games, and I think there is infinite potential to do so, but I was still happy with the variety those 4 provide.

<h1>Art</h1>
As I am not a very talented artist when it comes to drawing, I took a different approach to create the "3D" art for the project (such as the background to the Back to the Future game, or the weapon in the Ghostbusters game). I created a new 3D Unity project, build the scenes I wanted in 3D instead of drawing them, then took image captures of the angles that I wanted. I then added the new 2D images into The Everymovie, and I think the effect was successful, especially its use in the Back To The Future game.
This did cause a slight clash in art styles, however the game still looked visually interesting and that is what matters most.
![image](\assets\movieSpider.gif)
<h6>Losing makes the audience throw popcorn!</h6> 
<h1>Technical Details</h1>
In terms of technical details for the project, there is not much to talk about, as the game was quite simple and there was at no point concerns about performance.
I wanted the game to look pixelated where the screen was a constant pixel size, and I used a little trick to achieve this. My camera, pointed at the game, renders to a RenderTexture instead of the screen. Then, elsewhere in the Unity scene, there is a quad which presents the RenderTexture to another camera. This camera however has the Pixel Perfect attachment, meaning it will always have a constant pixelation effect. The reason I did this was because having the standard camera with the pixel perfect attachment was causing issues in how things were scaled and rendered, and my workaround solved these issues. I think the end result was successful in what I wanted the game to be visually, and the game still performed adequately.

Making the game run on the web was very easy, as Unity has support for WebGL builds, as long as the game does not use any unsupported features such as Compute Shaders.

![image](\assets\movieGhoul.gif)
<h6>Ghoulbusters minigame.</h6> 

<h1>What went well</h1>
Winning the jam was a good feeling, and made me feel even more proud of what I managed to create. The way I handled going from minigame to minigame was quite intuitive to add new minigames: make a new prefab, make sure it has a "Minigame" script, and thats essentially all that was required. As long as somewhere in the minigame the event to end the minigame was called, it was valid.
I was also quite happy with the music (even though the minigame tracks were just slight variations on the actual movie soundtracks), especially the original sound effects that I made. The only audio I did not create was the sound effect of the car turning in the Back to the Future minigame.

Additionally, I made this game during my undergraduate dissertation, which I thankfully still managed to do very well on, and as such I'm pround I managed to successfully balance both projects.
<h1>What I would improve</h1>
My main improvement would come from adding more games to the project, as the game currently gets quite stale quickly. There is also some art which is placeholder, such as the win and loss screens.

In terms of the code for the project, I am relatively happy. All the code worked as intended, though it was a little specific to each game and not very modular. I could have programmed the minigames in a way which allowed for faster creation of new ones, but this could have limited the types of gameplay I could do for each minigame, and it would have also taken away from the already limited amount of development time.

Quite a lot of time on the project was spent doing art, as I am not a very competent artist.

Apart from these things, I would say I was very happy with this project.