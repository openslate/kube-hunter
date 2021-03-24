@Library('OpenSlateProd')_  // https://github.com/openslate/jenkins-shared-library

def deployWhen = {
    return (env.GIT_BRANCH == 'main' || env.GIT_BRANCH == 'develop')
}

def getDeployEnv = {
    if (env.GIT_BRANCH == 'main') {
        return 'prod'
    }
    else {
        return 'dev'
    }
}

openslatePipeline {
    mentions = '<@UB22LFDEJ>'
    deployEnv = getDeployEnv
    publish = publishWhen
    deploy = publishWhen
}
