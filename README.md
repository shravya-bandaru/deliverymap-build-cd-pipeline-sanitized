# Deliverymap Service Build/CD Pipeline Package (Sanitized)

Complete build and CD pipeline package for concourse-deliverymap-svc.
Includes all pipeline definitions, templates, and configuration files.
All sensitive values (IDs, secrets, passwords, tokens, keys, service accounts) are sanitized.


## Package Details

**Created:** 2026-02-03 09:20:14

## Sanitization

This package contains SANITIZED data. Configuration values with keys matching these patterns have been replaced with 'sanitized':

- Keys containing `id`
- Keys containing `secret`
- Keys containing `password`
- Keys containing `token`
- Keys containing `key`
- Keys containing `US_`
- Keys containing `storage_account_name`
- Keys containing `_host`
- Keys containing `_url`
- Keys containing `_uri`
- Keys containing `_user`
- Keys containing `service_accounts`
- Keys containing `pwcglb.com`
- Keys containing `pwcinternal.com`
- Keys containing `pwc.com`

### Example Sanitized Keys:
- `client_id` → `"sanitized"`
- `CLIENT_ID` → `"sanitized"`
- `tenant_id` → `"sanitized"`
- `buildId` → `"sanitized"`

## Contents

This package includes files from the following repositories:

### ConcourseCore/k8s/concourse-deliverymap-svc/
- deployment.yaml (sanitized)
- hpa.yaml (sanitized)

### ConcourseCore/k8s/concourse-deliverymap-svc/configs/us-dev/
- concourse-deliverymap-svc.configmap.yaml (sanitized)

### ConcourseCore/k8s/concourse-deliverymap-svc/configs/us-int/
- concourse-deliverymap-svc.configmap.yaml (sanitized)

### ConcourseCore/k8s/concourse-deliverymap-svc/configs/us-perf/
- concourse-deliverymap-svc.configmap.yaml (sanitized)

### ConcourseCore/k8s/concourse-deliverymap-svc/configs/us-qa/
- concourse-deliverymap-svc.configmap.yaml (sanitized)

### ConcourseCore/k8s/microservice-template/
- service.yaml (sanitized)
- deployment.yaml (sanitized)

### administration/scripts/bash/
- bake-secretmap.sh

### administration/scripts/python/utilities/
- get-secrets-from-yaml.py
- requirements.txt

### digital-cicd/pipelines/
- pipeline-v3.0.yaml (sanitized)

### digital-cicd/templates/jobs/
- build-base.yaml
- build-nx.yaml
- build-npm.yaml
- build-docker.yaml
- deploy-stage.yaml
- deploy-stage-jobs.yaml
- deploy-k8s.yaml
- deploy-base.yaml
- tag-deployment.yaml
- prepare-deploy.yaml
- approval-emails.yaml
- scan-base.yaml
- scan-blackduck.yaml
- scan-twistlock.yaml
- scan-secrets-detection.yaml
- scan-sonar.yaml
- scan-veracode.yaml
- scan-veracode-pipeline-scan.yaml
- scan-git-lint.yaml
- qa-base.yaml
- qa-shell.yaml

### digital-cicd/templates/stages/
- init.yaml
- ci.yaml
- cd.yaml
- cd-stage.yaml
- scan-with-defaults.yaml
- scan.yaml

### digital-cicd/templates/steps/
- deploy-base-steps.yaml
- steps-common-prepare.yaml
- k8sValidation.yaml
- replace-variables.yaml
- package-docker.yaml
- upload-jfrog.yaml
- steps-download-pipeline-artifact.yaml
- download-jfrog.yaml
- task-vault.yaml
- steps-docker-add-tag.yaml
- git-version.yaml
- steps-preview-pipeline.yaml
- mock-build.yaml

### tech-enablement-devops/pipelines/backend/
- monorepo-cd.yaml (sanitized)

### tech-enablement/.azure/
- cd-concourse-deliverymap-svc.yaml (sanitized)

### tech-enablement/config/
- docker.k8.yml (sanitized)

## Usage

Extract the package:
```bash
tar -xzf deliverymap-build-cd-pipeline-sanitized.tar.gz
```

View contents:
```bash
tar -tzf deliverymap-build-cd-pipeline-sanitized.tar.gz
```

## Source Specification

This package was generated from a YAML specification file that defines:
- Source file locations
- Destination paths in the tarball
- Which files to sanitize
- Sanitization patterns

To regenerate this package, use:
```bash
uv run --script create_pipeline_package.py --spec <spec-file.yaml>
```

## Additional Notes

This package contains everything needed to understand the build and deployment
pipeline for the deliverymap service, including:
- Azure DevOps pipeline definitions
- Pipeline templates from multiple repos
- Kubernetes manifests
- Configuration files

This sanitized package is safe for analysis and documentation purposes.

