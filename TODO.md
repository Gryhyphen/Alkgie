# TODO List of things I want to add

- Add enrichers/enhancers (things that add metadata)
    - Alkgie-GithubStarEnricher (adds metadata for the stars on github an entry has based on the url of source entries)
    - Alkgie-TimelineEnricher (adds metadata for when entities were first created (i.e. React went open source in 2013, svelte 2016 ))
        - Probably use iso timestamps
    - These examples of enrichers show that
        - Enrichers add metadata to AlkgieV1Entities (currently only entity-level, not sourceentry-level)
        - Have access to entity and sourceentry level data for READ access.
        - Can enrich data either programmatically through an api (like for github stars)
            - OR through manual curation (i.e. manually keeping track of the timeline of things)
    - Alkgie-GithubTimelineStarsEnricher
        - Track popularity over time, so can compare stuff like increase in star counts over time.
        - Track commits/releases over time? Use github tags or commits to compute active development metrics?
    - Alkgie - SponsershipEnricher
        - Add information on corporate sponsorships that projects receive to help learn what companies are backing
          the project.



- Clean up deduplication code
    - Remove repeat of duplicate logic, extract the interface of the "isDuplicate" comparision predicate thing.
    - Maybe use a reducer?
    - (FUTURE): Use machine learning deduplication, like dedupe.py. (Pain tho since this is all polygot)
    -           Maybe could be done using powershell and installing the dedupe csv thing?
    -           Or executing the python via powershell.
    -           I really dislike python version management tho.