
# Tutorial for installing the Inline-Hologram Reconstruction software 

Install Anaconda 3.6 (latest version for windows).
Therefore follow the tutorial in this link: [Anaconda Installation](https://docs.anaconda.com/anaconda/install/) (external). 

0. After you've installed Anacoda, download the ipython notebook file: ```Listings_1_ReconHoloInline.ipynb``` by clicking this [link](./Listings_1_ReconHoloInline.ipynb) and type control+s for saving it somewhere on the computer
<p align="center"><img src="./IMAGES/Tut1.png" width="400"></p>

1. Copy Image in the same folder as the ```.iypnb```-file
<p align="center"><img src="./IMAGES/Tut2.png" width="400"></p>

2. ```Windows+R``` => Run prompt
3. enter ```CMD``` and hit enter
4. The Terminal opens 
5. Copy the path where you have the image and script file (e.g. C:\Users\diederichbenedict\Downloads\HOLOGRAM)
<p align="center"><img src="./IMAGES/Tut3.png" width="400"></p>
6. Enter: cd "C:\Users\diederichbenedict\Downloads\HOLOGRAM" (or whatever path; right click is paste in the terminal)
<p align="center"><img src="./IMAGES/Tut4.png" width="400"></p>
7. Type "ipython notebook" -> enter
<p align="center"><img src="./IMAGES/Tut5.png" width="400"></p>
8. Browser opens at http://localhost:8888 (copy paste if not opening automatically)
9. Go to the field "Define experimental parameters" and change the variable name "my_holo_file" to the filename you acquired (e.g. "hologram_mouse.jpg"
<p align="center"><img src="./IMAGES/Tut6.png" width="400"></p>
10. Go to Cell and hit "run all" and keep your fingers crossed!! 
11. Vary the position of the slider in the 
<p align="center"><img src="./IMAGES/Tut7.png" width="400"></p>



If you're not happy with the region of interest (ROI) change the center coordinates ```center_x``` and ```center_y``` to what you would like to see in the RAW-hologram. 
Rerun the programm by hitting "run all" 

If you want to process a bigger field of view or ROI change the variable "mysize" to a bigger number, but take into account, that the processing time increasing!

If you think, that the refocussing range is either too small or too large (i.e. too close or too far away), than change the parameters:

```
# Creating costume widget
FocusSlider = widgets.FloatSlider(
    min = 0,
    max = .01,
    step = 1e-3,
    value=0,
    description = 'ZPos',
    continuous_update = True
)
```


```min```, ```max``` and step which describe the minimal/maximal focal distance between the sensor and the sample as well as the stepsize where the algorithm calculates the refocussed hologram.