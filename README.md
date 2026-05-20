# poolantir-toilet-simulation

<p align="center">
  <img src="img/logo.svg" alt="Poolantir" width="900" />
</p>

### Description
Proof-of-Concept of simply adding a data layer to bathrooms to track usage, using ML to detect restroom anomalies to optimize janitorial scheduling and improve restroom conditions.

---

### Project Tags
<div align="left">
  <img src="tags/uiowa.svg" width="123" alt="Uiowa" />
  <img src="tags/agentic.svg" width="129" alt="Agentic" />
  <img src="tags/firebase.svg" width="204" alt="Firebase" />
  <img src="tags/figma.svg" width="60" alt="Figma" />
  <img src="tags/python.svg" width="60" alt="Python" />
  <img src="tags/flask.svg" width="60" alt="Flask" />
  <img src="tags/react.svg" width="60" alt="React" />
  <img src="tags/esp.svg" width="60" alt="ESP" />
  <img src="tags/cpp.svg" width="60" alt="ESP" />
  <img src="tags/platformio.svg" width="60" alt="Pio" />
  <img src="tags/fusion.svg" width="60" alt="Fusion360" />
  <img src="tags/powerpoint.svg" width="60" alt="Powerpoint" />
  <img src="tags/bambu.svg" width="180" alt="Bambu Studio" />
</div>

---

## Project Idea

Our project is a non-invasive proof-of-concept that demonstrates
how adding a layer of data analysis to existing self-flush toilets can
optimize maintenance schedules and automate incident reports,
thereby promoting cleaner restrooms. Data is collected using a 3D
simulation; This is not a marketable solution. 

There are two goals:
- optimize janitorial schedules by detecting anomalies using ML --> improve restroom cleanliness
- give restroom users the information necessary to make correct restroom guesses so they do not have to wait --> improve user experience

We are simply using data to build a historical usage model of restrooms which ML model will use to 
detect anomalies. Here is a situation of an anomly at popular bathroom with 3 urinals over a one hour timeframe:

Historical Data (30 minutes, 50 uses):
- Urinal_1 used ~30%; 15 uses
- Urinal_2 used ~2%; 1 use
- Urinal_3 used ~68%; 34 uses 

Actual Data (30 minutes, 30 uses):
- Urinal_1 used ~60%; 18 uses (+30% change)
- Urinal_2 used ~33%; 10 uses (+31% change)
- Urinal_3 used ~6.7%; 2 uses (-61.3% change)

An ML model with sufficient historical data would be able to infer an anomaly at Urinal_3, which is historically the 
most used toilet, but currently the least used.

Additionally, historical usage and current trends can be used to inform users of optimal toilet to use. For example, if you
are tailgating at the University of Iowa library on a football game day, there are two locations you can go to use the restroom: 
- porta-potties (10-100 steps)
- library bathroom (a few hundred steps)

For example, if the porta-potties are extremely busy, you will spend more time waiting in line than it would take to walk a bit further to the library to use a 
restroom. This is a small anecdotal example, but the same idea applies to highly congested areas: airports, campuses, stadiums, etc. Think about if you get off a flight, have a short 
layover and are expected to board in 5 minutes. There may be multiple bathrooms you could use, but which is the best? A simple system like this would work wonders.

Ultimately, using the restroom is a sacred time and one that is not to be meddled with. In my honest opinion, there are few letdowns worse than really needing to use a toilet, only to 
walk into a restroom to find that they are all full.

## Project Images

<p align="center">
  <img src="img/poster-arch.svg" alt="System architecture" width="600" />
  <p align="center"><strong>Project Architecture</strong></p>
</p>

<div style="display: flex; flex-direction: row; justify-content: space-between; align-items: center; gap: 8px;">
  <div style="display: flex; flex-direction: column; align-items: center;">
    <img src="img/poster-iso.png" alt="Simulation Model" width="400"/>
    <p align="center"><strong>Simulation Model</strong></p>
  </div>
  <div style="display: flex; flex-direction: column; align-items: center;">
    <img src="img/digital-twin.png" alt="Digital Twin" width="400"/>
    <p align="center"><strong>Digital Twin</strong></p>
  </div>
</div>


## Project Demo

<div align="center">
  <a href="img/Poolanitr_Demo.mp4" title="View Demo Video">
    <img src="img/demo_thumbnail.png" alt="Demo" style="cursor: pointer;"/>
  </a>
  <p align="center"><strong>Click the image above to view the <a href="img/Poolanitr_Demo.mp4">Demo Video</a> (the .mp4 file is too large to display here)</strong></p>
</div>

## My Contributions
I was in charge of the project planning and simulation of data. I did not touch any of the ML / Data layer.

**Project Contributions:**
- 100% Idea, Project Architecture, and Planning
- 100% CAD Modeling, 3D Printing, and Project Assembly
- 100% Simulation Controller Software
- 100% Hardware Selection, PCB, and Microcontroller Software
- 75% Project Slidedeck (Abstract, Hardware, and Simulation sections) 
- 75% Project Poster (Abstract, Hardware, and Simulation sections)
- 0% Firebase Backend
- 0% Mobile Application
- 0% ML Detection Software

This project spanned three school weeks in which I spent ~150 total hours. The majority of the time was spent
working on the CAD model and 3D printing. Getting the glide perfect took many iterations of 
the diorama top/bottom frames and rack-and-pinion - plus a little bit of vasolene to remove the crunching noise. Wiring and soldering 
also took a large chunk of my time as there were six identical nodes to be soldered and custom adapters for my servo rails. 
About ~20 hours was spent agentically developing the frontend (simulation digital twin), backend (simulation behavioral model backend), and
the ESP32 nodes. Thankfully, I finished on time and hit all of my requirements which I set out to achieve. Given more time, I would make necessary 
changes to the software simulation portion of the project, writing it in C++. This would allow for better OOP modeling of the behavioral model and the use
of OpenMP to better simulated human behavior. A few all-nighters were pulled and many classes were skipped.

## Project Outcomes

Selected to present the project alongside Senior Design and other cool projects at the Uiowa ECE Modern Marvels event. 

<div align="center" style="display: flex; flex-direction: column; align-items: center;">
  <img src="img/group-photo.jpeg" alt="Group photo at Modern Marvels" style="margin-bottom: 16px;" />
  <img src="img/poster.jpg" alt="Project poster" />
</div>
<p align="center"><strong>Project Showcase</strong></p>
