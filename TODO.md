# 0.2.0 release

## done

* change licence to AGPL
* url parameters to pre-select fields
    - need to match these fields to the slugified field names
        - field names are no longer slugified from the labels but tied to field order in csv
    - need to ensure field names can be specified explicitly in case the column string ever changes
        - don't want urls in message boards with broken parameters
            - field names are no longer slugified from the labels but tied to field order in csv
            - field name drift is now less likely to happen
    - done
        - added a permalink widget that will always get you back to your selection
* 'reset' link
    - removes all selections
* basic styling
    - if column headers are centred, centre values
    - alternate row colours
    - done

* add some kind of process for updating comrades.csv
    - manage in this repository
    - on merge to master
        - compile javascript
        - copy compiled files to website
        - commit
        - split comrades.csv into two, maintained and not
            - create a branch on strongbox
            - update README
            - open a PR
    - done

## todo

* add link *back* to strongbox 'other addon managers'
* add description, declare bias
* add link for submitting an update
    - link should go to strongbox-comrades repo, not strongbox
* options available in dropdowns should become more limited as filters narrow
* CI
    - maybe investigate Github actions?
        - https://github.com/features/actions

## todo bucket

* update address bar with selected field changes so user can use 'back' button to undo selections
* add simplified no-javascript rendering
    - is this even possible in a SLA?
    - just a static will do
* replace booleans with ticks and crosses
    - preserve text label in dropdown
    - tick with caveat? 
        - "  ✓*  "
        - looks kinda shit
* group results
    - recursive grouping is fun, but lets limit this to one group at a time
        - 'platform' I think
* determine user's platform based on user agent (if windows, select windows, etc)
    - perhaps a standard platform profile? 
        - a 'windows' profile gets unambiguous windows 'yes', 'gui'
        - a 'linux' profile gets ambiguous linux 'yes*', 'f/oss' yes, etc
