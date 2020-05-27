
1. Create test namespace in kubernetes.

    kubectl create namespace test

2. First create the priority class.

    kubectl create -f priorityClass.yml

3. Create the deployment.

    kubectl create -f deployment.yml

4. Create disruption budget.

    kubectl create -f podDisruptionBudget.yml

5. Create hpa.

    kubectl create -f hpa.yml

6. Create service.

    kubectl create -f service.yml
