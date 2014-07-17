build-tools
===========

When building a distribution for downstream consumption:

Note: [all] works on all releases

1. Create your own corimf-settings from the sample provided.
1. [all] Optional: run corimf-setup for initial setup a new workspace with new repos.
1. Run corimf-catchup-apache to get your local repos and corimf up-to-date
   with the content and tags from the Apache repos.
1. Run corimf-newver to create a new ESR branch from an existing Apache branch
   and put it on corimf.
1. Make your changes to the ESR branch, commit them and push them to corimf.
1. Run corimf-catchup to get your local repos up-to-date from corimf, if more
   than one person is contributing to a single fix.
1. [all] Run corimf-check to sanity check everything.  This needs to be run in the git repo ( for example 'cordova-ios')
1. [all] Run corimf-show-plugin-versions to verify that the present versions of the plugins are what is desired (match what the platforms were tested against by the community)
1. [all] Run corimf-tag to create a new tag on the branch
1. Run corimf-cron to verify that the cron job syncing git-wip-us.a.o with
   github.com/apache is running well.
1. Run corimf-snapshot to create a zip of each platform source.
1. Run the platform build scripts
   - corimf-build-android

