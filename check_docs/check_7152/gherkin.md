Description:
    Checks if a domain has privacy protection enabled
    This check will FAIL if a domain has privacy protection disabled

Scenarios:
 Scenario 1:
      Given: There are no Route53 Domains in the Account
       Then: PASS
 Scenario 2:
      Given: There are Route53 Domains in the Account
        And: For each Domain check
        And: Privacy Protection is enabled
       Then: PASS for that domain
 Scenario 3:
      Given: There are Route53 Domains in the Account
        And: For each Domain check
        And: Privacy Protection is disabled
       Then: FAIL for that domain