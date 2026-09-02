# Sidequest
Final project for the Building AI course
# Sidequest

Final project for the Building AI course

## Summary

A travel app that builds itineraries based on what you actually like instead of the same "Top 10 things to do" list every site shows. You describe what you want and it matches you to real places, then builds a day-by-day plan.

## Background

Every travel site has the same top 10 list for every city, made for the average tourist, not for you. Problems with this:

* Doesn't take into account what you actually want - quiet vs busy, food vs museums, slow vs packed schedule
* The more a place is on these lists, the more it gets recommended, so smaller/better places never get a chance
* Planning something more personal yourself means hours of reading blogs and forums

I like this idea because I'm tired of seeing the same top 10 lists everywhere and wanted to think about a way around that.

## How is it used?

You tell the app what you're looking for, e.g. "quiet nature spots, good coffee, avoid tourist traps, 4 days in Lisbon." It matches your preferences against place descriptions/reviews using NLP, ranks places by fit instead of popularity, and builds a day-by-day plan around the best matches.

Mainly for people planning their own trips who feel like the standard tourist route isn't really their thing.

## Data sources and AI methods

Would need travel review text and open map data (place info, hours, travel times). AI-wise: TF-IDF/text vectors to compare preferences against place descriptions, nearest neighbor to find the best matches, and some constraint-based scheduling for the day plan.

Built a small working demo (`demo.py`, plain Python, no libraries) that does the TF-IDF + nearest neighbor matching on a few made-up places. Running it with "quiet calm local spots avoid crowds good coffee" ranks the quiet local spots above the busy famous landmarks.

## Challenges

Need more thought on this. Data goes stale, reviews are biased toward whoever writes them, and if this got popular the "hidden gems" would just become the new crowded spots.

## What next?

Right now it's just an idea plus a small demo. Would need real data sources, user feedback to improve the model, and a prototype for one city to test if it actually works.

## Acknowledgments

* Inspired by being tired of generic top 10 travel content
* Course concepts (nearest neighbor, TF-IDF, hill climbing, overfitting) from the Building AI course
* Building AI course project
