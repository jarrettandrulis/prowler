Description:
    Checks if a domain has a domain transfer lock enabled.
    This check will FAIL if a domain has a transfer lock disabled (clientTransferProhibited not set in the domain statusList)

Scenarios:
 Scenario 1:
      Given: There are no Cache Clusters in the Account
       Then: Return NOT_APPLICABLE
 Scenario 2:
      Given: There are Cache Clusters in the Account
        And: For each Cache Cluster check
        And: ReplicationGroupId is not null or empty
       Then: Return NOT_APPLICABLE for that Cache Cluster