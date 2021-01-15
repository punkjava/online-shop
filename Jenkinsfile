node{

    stage('SCM Checkout')
    {
        git credentialsId: 'ce98fbf8-3a99-4ec6-86a5-9dc6803f0e97', url: 'https://github.com/punkjava/online-shop.git'
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
             
             sh 'docker login -u "punkjava" -p "pankaj123" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'docker push punkjava/jenki'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
