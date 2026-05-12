---
layout: default
---

<div align="center">
<img src="https://github.com/inland-thempire/poetry-publishers/blob/master/pritchard-untitled-boom-recto.png" alt="Text reading: Boom!">

 
  <i>Untitled (Boom!)</i> (undated) by N.H. Pritchard
</div>

# Mapping Poetry Publishers into the 21st Century

## Introduction

Poetry is an art closely bound to its physical presentations and modes of distribution: particularly in the world of small press publishing, the book is a container which transmits a poetics of its own. Yet a material poetics bears material costs, and poetry publishers are tasked with balancing aesthetic ambitions with the realities of disseminating art under late capitalism. How, then, are networks of distribution impacting avenues to disseminating a book of poems?

This project collocates data about poetry publishers to explore how recent commercial and historical phenomena impact the art form. Gleaned from the [Community of Literary Magazines and Presses' Directory of Publishers](https://www.clmp.org/readers/directory-of-publishers/), its principle dataset is presented on a map that displays each publisher according to the year they were founded. A supplementary chart reflects the types of distributors these presses are now using (most notably Asterism, which rose to replace Small Press Distribution). These metrics allow for a visualization of what avenues (from book to publisher to distributor to bookstore) are opened and foreclosed at recent turning points for the industry.

While this project includes poetry publishers based outside of the US, its main focus is upon publishers based in the US and its territories.

## Background

Poets and their circles have been anecdotally circling around a number of recent events that have had a significant impact on publishing, leading to the opening, closure, acquisition, and overhauls of many presses. Amid some general trends (including moves toward digital formats and print-on-demand), these watershed events are in dialogue with my project in particular:

*   **2013** - Major book distributor Ingram launches IngramSpark, offering print-on-demand and distribution as an alternative to traditional bulk offset printing (_IngramSpark_, 2023)
*   **March 2020** - COVID-19 prompts a widespread shutdown of non-essential commerce; some poetry publishers cease sales and operations (_Publishing During a Pandemic_, 2020)
*   **March 2024** - Small Press Distribution, the main distributor of many small press publishers, shutters overnight, leaving many publishers scrambling to send out books to retailers (_About the Closure of Small Press Distribution_, 2025)
*   **May 2025** - The Trump administration terminates or withdraws National Endowment for the Arts (NEA) grants for around 40 independent and nonprofit poetry publishers (_The NEA Defunded us. Now what?_, 2025)


### Poetry Publishers Mapped by Year Established (1947-Present)

<p align="center">
<img src="https://github.com/inland-thempire/poetry-publishers/blob/master/publisher_year_animation.gif" alt="animated publisher map with names appearing by year" width="700">
</p>

  
## Workflow

*   I began by web scraping CLMP’s publisher database to collect data about publishers' genres, founding dates, locations, and distributors
*   Next, I saved this publisher data to a CSV using ‘pandas’ python library
*   I tabulated and cleaned the data in OpenRefine to allow me to manipulate the data according to standardized years and places
*   I reconciled the publisher dataset with CLMP's 2025 report, [Presses Formerly Distributed by SPD: Where They Are Now](https://www.clmp.org/about-the-closure-of-small-press-distribution-faqs/presses-formerly-distributed-by-spd-where-they-are-now/)
*   I generated coordinates for publisher locations using ezGeocode
*   I mapped publishers in QGIS for easy visualization
*   Returning to 'pandas', I created a pie chart to represent the various distributors that publishers are now using

## Tools Used

*   'Requests' python library
*   'Pandas' python library
*   OpenRefine
*   ezGeocode
*   QGIS

## Further Uses

This list contains a finite number of active poetry presses, many of which are rapidly shifting their output and modes of distribution. This project may be expanded by adding additional publisher data through WikiData or through surveys of individual publishers. While more difficult to procure, broad data about the closure of poetry presses would also augment a quantification of changes in the publishing landscape. Additionally, data around submissions and payments for writers would link information about fees and distribution, allowing writers to get a clear picture of the full terms by which their work will be published.

## Files List

1. clmp_database.ipynb - Python notebook scraping CLMP’s publisher database
2. clmp_publishers.csv - CSV saving data from CLMP databse
3. clmp_publishers_cleaned.csv - CSV after cleaning data in OpenRefine
4. publishers_joined_dataset.csv - CSV after cross-checking distributor information with list from SPD's closure and with coordinates generated from ezGeocode
5. publisher_map.html - Map of publishers using QGIS from ezGeocode coordinates for web browser
6. publisher_map.qgz - QGIS file for map of publishers from ezGeocode coordinates
7. publisher_year_animation.gif - Gif of publishers appearing over time from QGIS mapping
8. publisher_charts.ipynb - Python notebook displaying distributors as a pie chart

* * *

## Sources

_About the Closure of Small Press Distribution._ (2025, October 27). Community of Literary 
  Magazines and Presses. (https://www.clmp.org/about-the-closure-of-small-press-distribution-faqs/)
  
_IngramSpark: A Decade of Amplifying Indie Authors and Publishers._ (2023). PublishersWeekly.com. (https://www.publishersweekly.com/pw/by-
  topic/industry-news/publisher-news/article/93461-ingramspark-a-decade-of-amplifying-indie-authors-and-publishers.html)

_The NEA Defunded Us. Now What?._ (2025, May 5). Deep Vellum. Deep Vellum. (https://www.deepvellum.org/news/nea-termination)

_Presses Formerly Distributed by SPD: Where They Are Now_ (2025, June 9). CLMP. (https://www.clmp.org/about-the-closure-of-small-press-distribution-faqs/presses-formerly-distributed-by-spd-where-they-are-now/)
  
_Publishing During a Pandemic: The Effects of COVID-19 on the Business of Books._ (2020, June 10). Poets & Writers. 
  (https://www.pw.org/content/publishing_during_a_pandemic_the_effects_of_covid19_on_the_business_of_books)

