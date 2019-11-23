---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "ALWL"
summary: "The project I made for the Fabacademy 2019"
authors: []
tags: [Fablab]
categories: []
date: 2019-07-14T00:32:47+03:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
 - name: Project
   url: http://fabacademy.org/2019/labs/oulu/students/alok-sethi/projects/final-project/
   icon_pack: fas
   icon: graduation-cap

 - name: Fablab home page
   url: http://fabacademy.org/2019/labs/oulu/students/alok-sethi/
   icon_pack: fas
   icon: graduation-cap

 - name: Git Repo	
   url: https://github.com/aloksethi/alwl/
   icon_pack: fab
   icon: github

#url_code: "https://github.com/aloksethi/alwl/"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
[//]: # ( As I am still working on the project, I will list all the updates to it on this page.)
Finally, have a PCB with the ATmega328P. Gerber can be downladed from the Github. The designed board is a four layer board.
Unfortunaltey, I associated a wrong footprint with the programming header so cannot plug the programming cable from the Atmel ICE directly. 
Below are the images of how the header is actually placed and how it was supposed to be placed.


{{< figure  library="true" src="alwl/header_pcb_layout.JPG" title="Programming header in the layout"  numbered="true" lightbox-group="header" >}}
{{< figure  library="true" src="alwl/header_pcb_schm.JPG" title="Programming header in the schematic" numbered="true" lightbox-group="header" >}}
