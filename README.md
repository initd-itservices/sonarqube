# Initd IT SonarQube

![InitdITOnboardingService](/img/logo.png)

Sonarqube Ontraining Setup

## Tools and frameworks

1. Openshift Client

## Setup

**NB**: Before you set your project please have [openshift client](http://mirror.openshift.com/pub/openshift-v4/clients/ocp/latest/).

1. Validate Installation

    ```bash
    oc version 
    ```

    ```bash
    ./oc.exe version
    ```

2. Login to target cluster

    ```bash
    oc login -u <USERNAME> -p <PASSWORD> <CLUTER-API-URL>
    ```

3. Create namespace

    ```bash
    oc new-project <PROJECT-NAME>
    oc project <PROJECT-NAME>
    ```

4. Install Sonarqube 

    ```bash
    cd k8
    oc apply -f .
    ```

**NB** : Please you will probably be working in an enteprise enviroment which may not allow you install external tools like oc and may be using windows so just download the .exe file and place it in the route of the project


```bash
oc adm policy add-scc-to-user anyuid -z default -n <namespace>
```

Enjoy.

Project is Developed by **Initd**.
