---
layout: default
---

# Scanning Poetry Publishers

#### _Poetry is not a luxury, but it is a commodity._


## Introduction

Poetry is an art closely bound to its physical presentations and modes of distribution: particularly in the world of small press publishing, the book is a container which transmits a poetics of its own. Yet a material poetics bears material costs, and poetry publishers are tasked with balancing aesthetic ambitions with the realities of disseminating art under late capitalism—poetry is not a luxury, but it is a commodity. How, then, are networks of distribution impacting avenues to disseminating a book of poems?

This project collocates datasets—data about poetry publishers and bibliographic metadata about poetry publications—to explore how recent commercial and historical phenomena impact the art form. Gleaned from the Community of Literary Magazines and Presses website, its principle dataset is presented on a map with options to explore the data by founding year, distributor, and approximate volume of output. These metrics allow for a visualization of what avenues (from book to publisher to distributor to bookstore) are opened and foreclosed at recent turning points for the industry.

While this project includes poetry publishers based outside of the US, its main focus is upon publishers based in the US and its territories.

## Background

Poets and their circles have been anecdotally circling around a number of recent events that have had a significant impact on publishing, leading to the opening, closure, acquisition, and overhauls of many presses. Amid some general trends (including moves toward digital formats and print-on-demand), these watershed events are in dialogue with my project in particular:

*   **2013** - Major book distributor Ingram launches IngramSpark, offering print-on-demand and distribution as an alternative to traditional bulk offset printing (_IngramSpark_, 2023)
*   **March 2020** - COVID-19 prompts a widespread shutdown of non-essential commerce; some poetry publishers cease sales and operations (_Publishing During a Pandemic_, 2020)
*   **March 2024** - Small Press Distribution, the main distributor of many small press publishers, shutters overnight, leaving many publishers scrambling to send out books to retailers (_About the Closure of Small Press Distribution_, 2025)
*   **May 2025** - The Trump administration terminates or withdraws National Endowment for the Arts (NEA) grants for around 40 independent and nonprofit poetry publishers (_The NEA Defunded us. Now what?_, 2025)



![me](https://github.com/inland-thempire/poetry-publishers/blob/master/docs/publisher_year_animation.gif)


  
## Workflow

*   I began by web scraping CLMP’s publisher database to collect data about publishers' genres, founding dates, locations, and distributors
*   Next, I saved this publisher data to a CSV using ‘pandas’ python library
*   I tabulated and cleaned the data in OpenRefine to allow me to manipulate the data according to standardized years and places
*   I reconciled publisher data with supplemental datasets on output and distribution
*   I generated coordinates for publisher locations using ezGeocode
*   Finally, I mapped publishers in QGIS for easy visualization

## Tools Used

*   'Requests' python library
*   'Pandas' python library
*   OpenRefine
*   ezGeocode
*   QGIS

## Further Uses

This list contains a finite number of active poetry presses, many of which are rapidly shifting their output and modes of distribution. This project may be expanded by adding additional publisher data through WikiData or through surveys of individual publishers. While more difficult to procure, broad data about the closure of poetry presses would also augment a quantification of changes in the publishing landscape. Additionally, data around submissions and payments for writers would link information about fees and distribution, allowing writers to get a clear picture of the full terms by which their work will be published.

## Files List

1. clmp_all_data.ipynb - python notebook scraping CLMP’s publisher database
2. publisher_data.csv - CSV saving data from CLMP database
3. publisher_data_cleaned.csv - CSV after cleaning data in OpenRefine

* * *

## Sources

_About the Closure of Small Press Distribution._ (2025, October 27). Community of Literary 
  Magazines and Presses. https://www.clmp.org/about-the-closure-of-small-press-distribution-faqs/
  
_IngramSpark: A Decade of Amplifying Indie Authors and Publishers._ (2023). PublishersWeekly.com. https://www.publishersweekly.com/pw/by-
  topic/industry-news/publisher-news/article/93461-ingramspark-a-decade-of-amplifying-indie-authors-and-publishers.html

_The NEA Defunded Us. Now What?._ (2025, May 5). Deep Vellum. Deep Vellum. https://www.deepvellum.org/news/nea-termination
  
_Publishing During a Pandemic: The Effects of COVID-19 on the Business of Books._ (2020, June 10). Poets & Writers. 
  https://www.pw.org/content/publishing_during_a_pandemic_the_effects_of_covid19_on_the_business_of_books
