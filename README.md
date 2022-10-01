# Dev Setup

1. Create Python Environment:  
`python3 -m venv .venv`
2. Activate Environment:  
`source .venv/bin/activate `
3. Install requirements:  
`pip install -r requirements.txt`

# Misc
https://projectq.io/data/source/verses.csv
https://raw.githubusercontent.com/skeptic-x/projectq.io/gh-pages/data/source/verses.csv
# Build Site
`mkdocs build`
# Serve Site
`mkdocs serve`
# Deploy Site
`mkdocs gh-deploy -c -m "projectq.io website update." --force --no-history`