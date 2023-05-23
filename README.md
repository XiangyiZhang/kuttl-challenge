## Description
The policy adds the label "lfx-mentorship: kyverno" to ConfigMap resources in namespaces that start with "team-". This testsuite aims to validate the functionality of this policy.

## Expected Behavior

**testcase-a**: A test case to validate the normal behavior of the policy. The ConfigMap should be successfully muted. Note that this policy does not keep pre-existing labels on the resource.

**testcase-b**: A test case to ensure that the policy does not affect the ConfigMap without the desired match in namespace. The namespace is set as "default".

**testcase-c**: A test case to ensure that the policy does not affect resources other than ConfigMaps. The kind is set as "Pod".

**testcase-d**: A test case to validate that the policy will change the label of the ConfigMap to "kyverno" even if there is a pre-existing "lfx-mentorship" entry.
