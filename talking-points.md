---
Header:
  Left: ""
  Center: ""
  Right: "Solar Eclipse Lesson Speaking Notes"
Footer:
  Center: © {{ CurrentDate "yyyy" }} Grader Than Technology LLC
---

# Slides

## Slide 1 - "Solar Eclipse"

- A solar eclipse happens when the Moon moves between the Sun and Earth, creating a shadow on Earth.
- Solar eclipses are rare. The last total eclipse in America was in 2017.
- At least two solar eclipses occur each year somewhere on Earth.
- Total eclipses happen only during a new moon, about once every 1-2 years.


## Slide 2 - "What is an eclipse?"

- A solar eclipse occurs when the Moon passes between the Sun and the Earth, casting its shadow on Earth.
- People on earth that in the umbra (black circle) will see a total eclipse.
- Those in the penumbra (lighter orange/red circle)  will see a partial eclipse.
- Total solar eclipses, where the Sun and Moon appear the same size in the sky, are a special kind of eclipse.
- Typically, Earth experiences two solar eclipses each year, but total eclipses are rarer.
- As the Moon slowly drifts away from Earth, total solar eclipses will become even rarer and eventually cease.

## Slide 3 - "Types of Eclipse"

- This slide showcases the three main types of solar eclipses: partial, annular, and total.
- In a partial eclipse, the Moon only covers a part of the Sun, leading to a partial shadow on Earth.
- An annular eclipse occurs when the Moon is directly in front of the Sun but doesn't completely cover it, creating a "ring of fire" appearance. 
- Annular eclipse happens when the moon's orbit is further from the earth so the moon appears smaller from perspective of an observe on earth.
- During a total eclipse, the Moon fully covers the Sun, plunging a specific area on Earth into darkness.

## Slide 3 - "Eclipse Path"

- The image shows the path of the eclipse across America on April 8th, 2024.
- The dark, thicker line represents the umbra, where viewers will see a total eclipse.
- The thinner lines illustrate the penumbra, indicating areas that will experience a partial eclipse.

<div class="page"></div>
&zwj;

# Notebook

## Code Cell 1 - "Install Dependencies"

Before you begin make sure your students run this code cell so all the python
packages are installed.

## Code Cell 2 - "Moon's Orbit in 3D"

- The provided code snippet generates a 3D visualization of the Moon's orbit around the Earth, specifically for April 8th, 2024, in anticipation of the next solar eclipse.

1. **`att_moon = 384_400 * u.km`**
   - This variable tells us the average distance from the Moon to the Earth, which is 384,400 kilometers. Imagine stacking 384,400 one-kilometer rulers end to end; that's how far the Moon is from us!

2. **`ecc_moon = 0.0549 * u.one`**
   - This is the Moon's orbital eccentricity, which measures how much the orbit deviates from a perfect circle. A value of 0 would be a perfect circle, but 0.0549 means the Moon's orbit is slightly oval-shaped.

3. **`inc_moon = 5.145 * u.deg`**
   - This is the inclination of the Moon's orbit, measured in degrees. It tells us the Moon's orbit is tilted 5.145 degrees relative to Earth's equator. If Earth's equator was a flat line, the Moon's path tilts a little bit off this line.

4. **`raan_moon = 0 * u.deg`**
   - RAAN stands for Right Ascension of the Ascending Node. This complicated term just means where the Moon's orbit crosses the Earth's equatorial plane going north. Here, it's set to 0 degrees, but usually, this number helps track where that crossing point is in space.

5. **`argp_moon = 0 * u.deg`**
   - This is the argument of perigee, which tells us where the closest point of the Moon's orbit is to Earth, in relation to its orbit. Since it's set to 0 degrees, it's used as a starting point for measuring the orbit's shape.

6. **`nu_moon = 0 * u.deg`**
   - Nu represents the true anomaly, which is where the Moon is on its orbit at a specific time. At 0 degrees, it means we're starting our measurements from a specific point in the Moon's orbit.

### Try it out

- Have the students change the `att_moon`, `ecc_moon`, or `inc_moon` and see what happens to the orbit.

<div class="page"></div>
&zwj;

## Code Cell 3 - "Moon Orbiting the Earth Animation"

- This section introduces a 2D animation that accurately depicts the Moon's orbit around the Earth over a year, completing about 13.37 orbits.
- Using Python libraries such as Matplotlib and Poliastro, the code creates a dynamic visualization of the Moon's journey.
- The animation parameters are set to reflect the true dimensions and distances, including the Moon's orbit's semi-major axis and eccentricity.
- A detailed setup for the plot includes Earth and Moon representations, with specific adjustments for visual clarity and scale.
- The animation function updates the Moon's position daily, offering insights into its orbit's dynamics and the number of rotations around the Earth.


## Code Cell 3 - "Visualizing Earth's Orbit Around the Sun in 3D"

- This section offers a 3D visualization of Earth's orbit around the Sun, aiming to convey the concept of Earth's annual journey despite the scale being symbolic.
- The code utilizes the Poliastro library to create a dynamic 3D model, highlighting Earth's orbit at a significant average distance of 150 million kilometers from the Sun.
- By employing an interactive 3D plotting tool, the simulation provides an immersive experience to understand Earth's position and movement in space.
- The simulation also illustrates the tilt of Earth's axis and its inclined orbit, explaining the seasonal changes and varying solar exposure experienced on Earth.
- This educational tool demonstrates the intersection of astronomy and Python programming, offering a visually engaging method to explore celestial mechanics.

### Try it out

The students can add another planet by importing a new planet by name. Make sure
the name is capitalized. Then adding the imported planet to the frame. Belows
are the code additions for adding Mars.

```py
from poliastro.bodies import Earth, Sun, Mars <- Added Mars
...

frame.plot_body_orbit(Mars, J2000, label=Mars) <- Add this to the end
```

## Code Cell 3 - "Simulating Solar Eclipse"

- This code demonstrates a simulation of the Moon's orbit around Earth with a symbolic Sun, illustrating how solar eclipses occur.
- Up to five solar eclipses (partial, annular, or total) can happen each year, visible from somewhere on Earth, with total eclipses only during the new moon phase.
- The visualization is not to scale; the Earth and the Moon are exaggerated in size to make the phenomena observable, while the Sun's size is significantly reduced.
- A dotted line between the symbolic Sun and Earth represents the potential path for solar eclipses, highlighting when the Moon crosses this line, signaling an eclipse event.

💡 TIP: If the animation is not working or glitching press the restart button at
the top of the notebook then run the cell again.
