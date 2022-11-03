# Eclipse SDV Hackathon on BCX2022

One-Pager ([PowerPoint](./assets/ZF_Poster_Hackathon_OnePager.pptx), [PDF](./assets/ZF_Poster_Hackathon_OnePager.pdf))

# Welcome to the OpenStreepMap :world_map: and CARLA :car: hack challenge!

Your goal is to **Drive a vehicle, any route of planet earth in a simulation environment**. The use case:

`As a SDV developer I want to put my software into a car that drives any specific route in any specific city with an effort comparable programming a navigation system like google maps.`

As a hack challenge for Eclipse SDV, it's a good use case to try out the involved technology and experience some of the challenges infusing real world data into a virtual world. And bringing a real world use case into a simulator.

In this hack challenge, you can

- **show how real world data can be brought into a virtual world running on a simulator**
- **show how vehicle can navigate from A to B in a virtual world** using technology and experience from open source projects
- **combine exciting open source technology** from geographic data, routing engines, simulators and automotive

The rough plan is to extract a city from OSM, convert into importable format for the simulator (provided by the simulator). A route on the imported virtual world is created and navigation steps from a routing engine navigates a virtual vehicle on the fastest way in the virtual world.

Validate the results by visualizing them with metrics from the vehicle and the simulator. If you wanna do a website showing it, do it :).

It's up to your hack team's creativity.

*Hint:* There are already several open source projects with good information and ideas

## Your hack team should have the following skills


- Some **development skills** in the programming language Python would be necessary to interfacing with APIs
- Besides from that, a Hacker would only need a notebook:
  - Windows (10 or 11)
  - Ubuntu (18.04 or newer)
  - Mac OS
- Network-Interface
  - ethernet port (1 Gbit)
  - wifi
- Remote instances with a graphics card running the simulator are provided
- To run the simulator locally on your machine a dedicated graphics is required
  - According to CARLA documentation CARLA aims for realistic simulations, so the server needs at least a 6 GB, but reducing the rendering resolution and quality settings allows also graphic cards with less memory (2-3GB)


[Step 1 - Setting up development environment and making first contact with CARLA](./docs/step-1-first-contact.md)

[Step 2 - Investigate data export from OpenStreetMap and import in CARLA](./docs/step-2-oh-my-osm.md)

[Step 3 - Familiarize with CARLA to understand the concept of an Actor](./docs/step-3-carla-rize.md)

[Step 4 - Investigate how to create a route using OSMR](./docs/step-4-navigate-me.md)

[Step 5 - Implement, test, and run your "virtual Uber service"](./docs/step-5-hey-uber.md)

Happy hacking!
