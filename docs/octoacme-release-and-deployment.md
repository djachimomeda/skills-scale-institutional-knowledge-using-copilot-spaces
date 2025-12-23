# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans (coordinated with DevOps Engineer)
- Release notes drafted
- Rollback / mitigation plan documented (prepared by DevOps Engineer)
- Smoke tests prepared
- Infrastructure and monitoring ready (verified by DevOps Engineer)
- Complete [DevOps Release Readiness Checklist](octoacme-devops-release-readiness-checklist.md)

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests (DevOps Engineer executes)
- [ ] Deploy to production (automated pipeline preferred, managed by DevOps Engineer)
- [ ] Run post-deploy verifications (DevOps Engineer monitors)
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (DevOps Engineer leads technical response)
  - Rollback to last known-good release if necessary (executed by DevOps Engineer)
  - Triage root cause and capture action items
  - Conduct post-incident retrospective with all involved roles

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
