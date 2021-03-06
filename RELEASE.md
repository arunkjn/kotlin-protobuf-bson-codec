Releasing
========
* Change the version in `gradle.properties` to a non-SNAPSHOT version.
* Update the `README.md` with the new version.
* `git commit -am "Prepare for release X.Y.Z."` (where X.Y.Z is the new version)
* `git tag -a X.Y.Z -m "Version X.Y.Z"` (where X.Y.Z is the new version)
* `./gradlew clean uploadArchives`
* Update the `gradle.properties` to the next SNAPSHOT version.
* `git commit -am "Prepare next development version."`
* `git push && git push --tags`
* Visit [Sonatype Nexus](https://oss.sonatype.org/) and promote the artifact.