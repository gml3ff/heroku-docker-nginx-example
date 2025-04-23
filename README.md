# tv-lupton-io

Website code for tv.lupton.io music project. 

## Background

This is a simple web project built using HTML & Javascript hosted on Heroku. It's essentially a video frame for a series of DJ mixes I have uploaded to Youtube with a "VHS feel." Audio from all DJ mixes was passed into Touch Designer to produce the audio-reactive visuals. More info can be found on the [project's about page](https://tv.lupton/about).


## Explanation of Pages

### Home (static-html/index.html)

Presents user with home page of options. 


### Watch Now (static-html/watch-now.html)

Automatically plays a mix corresponding to your browser's current time. There are 16 1.5 hour mixes that correspond to each point in the day. If you pause the video, it will skip forward the amount of time paused. If the video reaches the end of the 1.5 hr time block, the page should advance to the next video (still working out the kinks on this one). 

### TV Guide (static-html/tv-guide.html)

Allows you to select any one of the 1.5 hr slots at your convenience. I have listed the styles of each of these mixes below. All times are listed in 24 hour time to eliminate confusion. 

#### Daytime Program
- **06:00-07:30**: Ambient, Jazz, Rock, Balearic
- **07:30-09:00**: Jazz, Funk, Soul, New Wave
- **09:00-10:30**: Electronic, Downtempo, Rock, Jazz
- **10:30-12:00**: Hip Hop, Soul
- **12:00-13:30**: Boogie, Balearic, Soul
- **13:30-15:00**: Rock, Shoegaze, Post Punk
- **15:00-16:30**: Trip Hop, Downtempo, Instrumentals
- **16:30-18:00**: Boogie, Disco, Brazilian
- **18:00-19:30**: Balearic, Boogie, Disco, Funk
- **19:30-21:00**: Disco, Funk

#### Nighttime Program
- **21:00-22:30**: House, Electro
- **21:00-22:30**: House, Electro
- **22:30-00:00**: House, Breaks, Garage, Techno
- **00:00-01:30**: House, Breaks, Trance, Techno
- **01:30-03:00**: Jungle, Breaks, Trance
- **03:00-04:30**: Techno
- **04:30-06:00**: Techno, House

## Deployment Instructions
Install heroku if you have not done so already

`brew install heroku`.

Then `cd` into the directory and launch the container. You'll need Docker to be running, I recommend using [Docker desktop](https://www.docker.com/products/docker-desktop/).

```
git clone git@github.com:gml3ff/tv-lupton-io.git
cd tv-lupton-io
heroku container:login
heroku create
heroku container:push web -a aqueous-ocean-73765 
heroku container:release web -a aqueous-ocean-73765
heroku open
```
