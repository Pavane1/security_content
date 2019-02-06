# security-content
Contains a collection of security stories with their corresponding detection, investigative, contexual and support splunk searches

# Consumption
Can be consumed using:
* API (https://api.splunksecuritycontent.com)
* CLI

# Structure
`src/` - splunk content app source files, includes lookups, binaries, and defaul config files

# Developing

For getting pre-commit checks, install the hooks see below for steps:
1. Install circleci [CLI Tool](https://circleci.com/docs/2.0/local-cli/#installation)
2. create virtualenv and install requirements: `virtualenv venv && source venv/bin/activate && pip install -r requirements.txt`
3. install pre-commit `pre-commit install`

To test a local change to CI or build make sure you are running docker and then
`circleci local execute -e GITHUB_TOKEN=$GITHUB_TOKEN --branch <your branch>`

Please not that every commit in a pull request will be followed by a commit that updates the source files under `src/default` for the searches
