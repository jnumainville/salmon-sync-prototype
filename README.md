# salmon-sync

This is a Github Action that syncs a folder to a Google Cloud bucket using `rclone`.

```
inputs:
  source:
    required: true
    type: string
    description: 'The source artifact to sync.'
  destination:
    required: true
    type: string
    description: 'The destination directory to sync. Relative to the bucket.'
  project_number:
    required: true
    type: string
    description: 'The Google Cloud project number.'
  bucket:
    required: true
    type: string
    description: 'The Google Cloud bucket to sync to.'
  credentials:
    required: true
    type: string
    description: 'The Google Cloud credentials.'
  delete-artifact:
    required: false
    type: boolean
    description: 'Whether to delete the artifact after syncing. Default is true. Recommened if the artifact is large and not needed after syncing.'
    default: true
```