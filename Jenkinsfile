#!groovy

properties([
    buildDiscarder(logRotator(numToKeepStr: '10')),
    parameters([
        string(defaultValue: "", description: "AWS account name.", name: 'BUILD_ACCOUNT', trim: false)
    ])
])

@Library('amibuilder@master') _

amiBuilder([
    "BUILD_ACCOUNT"             : params.BUILD_ACCOUNT,
    post_build_steps            : this.&postbuild
])

def postbuild() {
    stage('Archive Artifacts') {
        progressLogger.record('Artifacts archive', "archive the artifacts here", "log")
    }
}
