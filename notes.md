## Notes

Uses declarative instructions
Tells the host how to end up, not how to do it.

### Deployment Models:
    - Master-Agent
        default checkin is 30 minutes
        Pull based - Agent checks in and pulls config from master
    - Standalone
        Used in Dev/POC

### Execution Flow
    Master is a node that controls config
    Agents communicate with Master with Certificates over 8140
    Agent sends data about current state (facts) to Master
    Puppet checks catalog against host current state
    Puppet then makes changes and reports back to master
