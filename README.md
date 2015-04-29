# Releaser

Releases artefacts from release candidates with one command. For use as part of a continuous delivery pipeline in which users can create a release from a development commit and create a tag in Github with one command. This automates numerous manual steps required to release an artefact with the existing [release](https://github.com/hmrc/release) scripts.

The release candidate is a published artefact in a Bintray HMRC release candidate repository. Releaser works by taking a release candidate, modifying the verion numbers in the Manifest and file names and uploading files back to Bintray. *All compiled files are not touched in this process*.  

There are release and release candidate repositories in Bintray HMRC for standard (maven) projects and sbt-plugins which are in the Ivy style.

### Building
`sbt assembly` will place releaser-assembly-x.x.x.jar in your target/scala-2.11/ directory

### Running
`java -jar target/scala-2.11/releaser-assembly-x.x.x.jar` artifact release-candidate-version release-version

### License
 
This code is open source software licensed under the [Apache 2.0 License]("http://www.apache.org/licenses/LICENSE-2.0.html").
