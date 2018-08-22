Usage Notes
================================
## Installation


## Pulling in data

#### Gathering LinkedIn data

Visit https://www.linkedin.com/psettings/member-data and request an archive
of profile data.

###### Warning
For the moment LinkedIn does not export all profile data.  For example,
it appears that Volunteer Experience and Awards are missing.

#### Use jmperez's converter

1.  Start a simple web server, e.g.
```bash
cd tools/linkedin-to-json-resume/src
npm run start
```
Note : the move to typescript has been creating trouble, so for now use `920ec37`

2.  Use page to parse LinkedIn data and download resume.json as `./data/linkedin_jsr.json`

3.  Convert to FRESCA format
```
./tools/HackMyResume/src/cli/index.js convert data/linkedin_jsr.json to data/linkedin.json -f FRESH
rm data/linkedin_jsr.json
```

## Building

To build a resume combining all data from the `data` directory

```
hackmyresume build data/*.json to out
```

## Themes

FRESH themes are Markdown based and support multiple output formats.

JSON Resume themes are mostly HTML-based.


### FRESH defaults

Hackmyresume comes pre-packaged with themes from [FRESH]( https://github.com/fresh-standard/fresh-themes).
Create modified versions by forking
from `frsh-standard/fresh-themes` on github.

### Getting new themes

Get and use new FRESH/jsonresume themes via npm
```
npm install jsonresume-theme-somename
npm install fresh-theme-somename
```

Browse online at
https://jsonresume.org/themes/


### Using new themes

To use an installed theme use the flag
```
hackmyresume ... --theme path/to/theme
```
