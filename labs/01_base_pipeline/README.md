# Create a base pipeline

This folder holds the files for the lab _Create a Base Pipeline_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Command line commands for steps:
- Step 1: Create an echo Task:
    After modifying the tasks.yaml, use below command
    kubectl apply -f tasks.yaml

- Step 2: Create a hello-pipeline Pipeline
    After modifying the pipeline.yaml, use below command
    kubectl apply -f pipeline.yaml

- Step 3: Run the hello-pipeline
    Run the pipeline using the Tekton CLI:
    tkn pipeline start --showlog hello-pipeline

- Step 4: Add a parameter to the task
    After modifying the tasks.yaml, use below command
    kubectl apply -f tasks.yaml

- Step 5: Update the hello-pipeline to message-pipeline and change the config
    After modifying the pipeline.yaml, use below command
    kubectl apply -f pipeline.yaml

- Step 6: Run the message-pipeline
    Run the pipeline using the Tekton CLI:
    tkn pipeline start hello-pipeline \
    --showlog  \
    -p message="Hello Tekton!"

- Step 7: Create a checkout Task
    After adding the new task below the first one, use below command
    kubectl apply -f tasks.yaml

- Step 8: Create the cd-pipeline Pipeline
    After adding the new pipeline in the pipeline.yaml, use below command
    kubectl apply -f pipeline.yaml

- Step 9: Run the cd-pipeline
    Run the pipeline using the Tekton CLI:
    tkn pipeline start cd-pipeline \
    --showlog  \
    -p repo-url="https://github.com//nzkksdemo/wtecc-CICD_PracticeCode.git" \
    -p branch="main"

- Step 10: Update the cd-pipeline Pipeline
    After adding the new tasks in the pipeline.yaml, use below command
    kubectl apply -f pipeline.yaml

- Step 11: Run the cd-pipeline
    Run the pipeline using the Tekton CLI:
    tkn pipeline start cd-pipeline \
    --showlog  \
    -p repo-url="https://github.com/nzkksdemo/wtecc-CICD_PracticeCode.git" \
    -p branch="main"