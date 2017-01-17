# Read planner
Create reading schedules

## Components
- **Server**: Endpoints for interfacimng with Amazon books API and computing read time and generating schedules
- **Client**: Mobile app which the user interacts with
- **Chrome Extension**: Chrome extension which allows bookmarking pages and queuing them to the reading list

## Status
The server has the most preleminary work done so far for creating a proof of concept.

## Running locally

### Dependencies
- Node/Npm

### Running the project
1. Clone Repo
2. `npm start` (this will start the server and the mobile app inside the browser)

**Note**:
When cloning repo, make sure to pull in the submodules as well.

**NOTE 2**:
THe server won't actually run correctly locally since it depends on a valid AWS API key which I have not committed to the repo. To get it working, create a file `server/config/local.js` with the contents: 
```
module.exports = {
  globals: {
    aws: {
      accessKey: 'YOUR AWS ACESSD KEY',
      secretAccessKey: 'YOUR AWS SECRET KEY',
      associateTag: 'YOUR AWS PRODUCT API AFFILIATE TAG'
    }
  }
};
```