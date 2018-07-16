# Sparrowdo::VSTS::YAML:Publish

Sparrowdo module to generate VSTS yaml steps to publish contents to Artifactory.

    $ cat sparrowfile

    # Builkd nuge6 package for project "CoollLib." located in $working-folder
    module_run "VSTS::YAML::Artifactory::Publish", %(
      build-dir => "build",
      target-repo => "local-nuget", # Artifactory target repository 
      contents-dir => "packages/", # directory with content to publish 
      endpoint => "artifactory-stage" # VSTS Artifactory name 
    );

    $ sparrowdo --local_mode --no_sudo

# Author

Alexey Melezhik

