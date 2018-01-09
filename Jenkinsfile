pipeline {
    agent any

    stages {
        stage('Comparar Navegaciones') {
			environment {
				KBDir = credentials('MTKBDir')
				GXPROGRAMDIR = credentials('GXPROGRAMDIR')
			}
			steps {
				echo '----- Comparo Navegaciones -----'
				build job: 'Compare-Navigations', parameters: [text(name: 'KBPath', value: "${KBDir}"),  text(name: 'GX_PROGRAM_DIR', value: "${GXPROGRAMDIR}")]
			}
		}
	}
}