---
layout: default
---

# Scanning Poetry Publishers

#### _Poetry is not a luxury, but it is a commodity._


## Introduction

Poetry is an art closely bound to its physical presentations and modes of distribution: particularly in the world of small press publishing, the book is a container which transmits a poetics of its own. Yet a material poetics bears material costs, and poetry publishers are tasked with balancing aesthetic ambitions with the realities of disseminating art under late capitalism—poetry is not a luxury, but it is a commodity. How, then, are networks of distribution impacting avenues to disseminating a book of poems?

This project collocates datasets—data about poetry publishers and bibliographic metadata about poetry publications—to explore how recent commercial and historical phenomena impact the art form. Gleaned from the Community of Literary Magazines and Presses website, its principle dataset is presented on a map with options to explore the data by founding year, distributor, and approximate volume of output.

While this project includes poetry publishers based outside of the US, its main focus is upon publishers based in the US and its territories.

## Background

Poets and their circles have been anecdotally circling around a number of recent events that have had a significant impact on publishing, leading to the opening, closure, acquisition, and overhauls of many presses. 

*   **2013** - Major book distributor Ingram launches IngramSpark, offering print-on-demand and distribution as an alternative to traditional bulk offset printing
*   **March 2020** - COVID-19 prompts a widespread shutdown of non-essential commerce; some poetry publishers cease sales and operations
*   **March 2024** - Small Press Distribution, the main distributor of many small press publishers, shutters overnight, leaving many publishers scrambling to send out books to retailers
*   **May 2025** - The Trump administration terminates or withdraws National Endowment for the Arts (NEA) grants for around 40 independent and nonprofit poetry publishers


  
## Workflow

*   Web scraped CLMP’s publisher database using ‘requests’ python library
*   Saved publisher data to a CSV using ‘pandas’ python library
*   Tabulated and cleaned data in OpenRefine
*   Reconciled publisher data with supplemental datasets on output and distribution
*   Generated coordinates for publisher locations using ezGeocode
*   Mapped publishers in QGIS

## Tools Used

*   'Requests' python library
*   'Pandas' python library
*   OpenRefine
*   ezGeocode
*   QGIS

## Further Uses

This list contains a finite number of active poetry presses, many of which are rapidly shifting their output and modes of distribution. This project may be expanded by adding additional publisher data through WikiData or through surveys of individual publishers. While more difficult to procure, broad data about the closure of poetry presses would also augment a quantification of changes in the publishing landscape.

## Files List

1. clmp_all_data.ipynb - python notebook scraping CLMP’s publisher database
2. publisher_data.csv - CSV saving data from CLMP database
3. publisher_data_cleaned.csv - CSV after cleaning data in OpenRefine

* * *

## Sources

About the Closure of Small Press Distribution: FAQ - Community of Literary Magazines and Presses. (2025, October 27). Community of Literary 
  Magazines and Presses. https://www.clmp.org/about-the-closure-of-small-press-distribution-faqs/
  
IngramSpark: A Decade of Amplifying Indie Authors and Publishers. (2023). PublishersWeekly.com. https://www.publishersweekly.com/pw/by-
  topic/industry-news/publisher-news/article/93461-ingramspark-a-decade-of-amplifying-indie-authors-and-publishers.html
  
Publishing During a Pandemic: The Effects of COVID-19 on the Business of Books. (2020, June 10). Poets & Writers. 
  https://www.pw.org/content/publishing_during_a_pandemic_the_effects_of_covid19_on_the_business_of_books
