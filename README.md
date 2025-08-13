# MappingHub
Mapping Hub

This project is responsible for Updating the Website contents using GitHub Actions.  It is currently a WIP to take over the role of the previous views/Travis CI pipeline.  

### To pull the submodules:
`git submodule init`
`git submodule update`

### Submodules/components
* elements - elements and metadata (see repo for more info)
* mappings - mappings and metadata (see repo for more info)
* views - Node.js code to build the website from elements + mappings.
* [.github/workflows](.github/workflows) - github actions to pull code, compile, deploy to Mappinghub.github.io
    * MappingHub.org redirects to Mappinghub.github.io or the physical ip of github.io site?
    * TODO: Ask David how this works
* [mappinghub.github.io repo](https://github.com/mappinghub/mappinghub.github.io) - this repo builds a static website that is deployed to the mappinghub.github.io repo

## Github Actions
See [official documentation and resources](https://github.com/features/actions)
Navigate to .github/workflows
* build-site.yml - this configuration script executes the build process
    * Currently builds on any code pushes to the repo.
    * I believe submodules should be manually to be set to the desired version instead of automatically updating to most recent master branches.
    * Currently, "blank"/null push to the repo to get it to rerun build script
    * Alternatively, these scripts and build process can be initiated in [Actions tab](https://github.com/mappinghub/MappingHub/actions)
* SubmodulesSync.yml - this configuration script helps to sync submodules.


## Secrets and Tokens
* These need to be configured and accessible by the build script.
See: https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-secrets
