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