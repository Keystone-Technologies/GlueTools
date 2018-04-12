# About

GlueVersion is a PowerShell module built to allow for easy version control for IT Glue flex assets. It is broken down into several tools, each with their own associated functions/cmdlets:

## Version Control

The version control toolbox allows one to keep a revision history for flexible assets, including the ability to see who authored a revision at what time. A "job" is configured to track changes to flex assets based on specific filters given in a job config file. Once set up, a service (GlueSync) runs periodically and polls the IT Glue API for changes to any flex assets that the job filter has in scope. If changes occur, the service adds that revision information to a flat-file database.

Functions are provided to:

- Create a job
- Snapshot current flex asset information
- View flex asset revision history
- View specific revisions
- Set API rate limits
- Set polling frequency

## Compare Tools

Tools to compare flex asset versions are provided. Specifically, diff and Glue Blame (similar to git blame) functionality is granted according to the following list:

- Diff two flex asset revisions
- List changes to a specific field over time
- Blame
  - See who modified a specific revision or changed a flex asset within a time-frame
  - See the revision change + author info for a specific field of a flex asset
