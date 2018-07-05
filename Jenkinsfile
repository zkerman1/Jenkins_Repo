node {
    ws("C:\Jenkins_Workspace_2") {
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'C:\\Users\\zkerman\\Documents\\Github\\makefile-for-c']]])
		stage('Build') {
			powershell '''$myPath=Get-Location
				$myPath=$myPath -replace \'\\\\\',\'/\'
				C:\\cygwin64\\bin\\bash --login -c "cd \'$myPath\'; make clean; make"'''
		}
    }
}
