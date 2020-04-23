#!groovy

@Library('amibuilder@master') _

amiBuilder([
    "BUILD_ACCOUNT"             : "viaduct09,
    post_build_steps            : this.&postbuild
])

def postbuild() {
    stage('Archive Artifacts') {
        progressLogger.record('Artifacts archive', "archive the artifacts here", "log")
    }
}
