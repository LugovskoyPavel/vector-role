
pipeline {
    agent any

    stages {
        stage('Build') {
            try {
     stage ("Molecule test") {
        /* Jenkins check out the role into 
        a folder with arbitrary name, so we need to
        let Ansible know where to find 'fluteansible' role*/
        sh 'mkdir -p molecule/default/roles'
        sh 'ln -sf `pwd` molecule/default/roles/fluteansible'
        sh 'molecule test'
     }
   } catch(all) {
      currentBuild.result = "FAILURE"
      throw err
   }
            }
       
    
}
