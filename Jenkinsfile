node {
    stage('SCM') {
		git changelog: false, poll: false, url: 'https://github.com/Pratik-Kiri/ssisPakgae.git'
    }
    stage('Database schema upgrade') {
        echo 'Upgrading target schema'
    }
    stage('Execute Package') {
		bat label: 'Executing package', script: 'dtexec /f .\\\\CICDVersion2\\\\CICDVersion2\\\\ImportPackage.dtsx /SET "\\"\\Package.Variables[User::SourceFile]\\"";"\\"C:\\Code\\Incoming\\\\'
    }
 }
