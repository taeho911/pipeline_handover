# pipeline_handover

## Git Workflow
### XFES
| STUP Purpose | Target dev branch | Target release branch | Target staging tag |
| ------------ | ----------------- | --------------------- | ------------------ |
| CT/RT        | develop_xx        | release/yyyymmdd_xx   | staging/xx         |
| ST           | develop           | release/yyyymmdd      | staging/xx         |

### Config
| STUP Purpose | Target branch |
| ------------ | ------------- |
| CT/RT        | yyyymmdd      |
| ST           | yyyymmdd_xx   |

## Pipelines
### Repo Management 1
| CT/RT                  | ST                          |
| ---------------------- | --------------------------- |
|                        | Merge latest master branch  |
|                        | Merge latest release branch |
| Merge project branches | Merge project branches      |
| Maven deploy           | Maven deploy                |

### Repo Management 2:
| CT/RT                 | ST                    |
| --------------------- | --------------------- |
| Create release branch | Create release branch |
| Change staging tag    | Change staging tag    |
| Request oitsuki work  | Request oitsuki work  |

### Staging Up:
| CT/RT                   | ST                      |
| ----------------------- | ----------------------- |
| Apply manifests         | Apply manifests         |
| Build images            | Build images            |
| Copy SP images for SAPP | Copy SP images for SAPP |
| Tag images              | Tag images              |
| Store manifests         | Store manifests         |

git:
  - merge
  - diff
  - log
  - revert
  - reset
  
mvn:
  - deploy
