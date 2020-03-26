* Setup account at https://boinc.bakerlab.org/
* Get your "Weak Account Key" at https://boinc.bakerlab.org/rosetta/weak_auth.php
* Get the project link for the project you want to compute for. In this case it's the Rosetta@Home project (http://boinc.bakerlab.org/rosetta) as they are doing Covid-19 work.
* Setup the boinc client
    ```
    git clone https://github.com/njmccorkle/docker-boinc.git
    cd docker-boinc
    docker-compose pull
    docker-compose up -d
    ```
* Attach the project to your boinc client
    ```
    docker exec boinc boinccmd --passwd 123 --project_attach http://boinc.bakerlab.org/rosetta WEAK_ACCOUNT_KEY
    ```
