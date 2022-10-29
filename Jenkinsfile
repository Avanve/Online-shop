node{

    stage('SCM Checkout')
    {
       // git credentialsId: '', url: 'https://github.com/Avanve/Online-shop.git'
        git credentialsId: '505fe3cd-87db-4716-a18d-76cb67fceee5', url: 'https://github.com/Avanve/Online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
       /* withCredentials([string(credentialsId: 'docker-pwd', variable: 'DockerHubPwd')]) {
      
            
}   */ 
         sh 'sudo docker login -u "aarchana" -p "DockerHubPwd" docker.io'
        sh 'sudo docker push aarchana/job1_web2.0'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
            // sh 'sudo docker push upasanatestdocker/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
