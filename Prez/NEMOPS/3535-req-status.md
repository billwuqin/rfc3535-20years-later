
>      Ease of use is a key requirement for any network management
>      technology from the operators point of view.

**Status Update**:
: This is still a valid requirement. It is
       even exacerbated with the amount of techniques and extensions
       that were specified since then.

>      It is necessary to make a clear distinction between configuration
>      data, data that describes operational state and statistics.  Some
>      devices make it very hard to determine which parameters were
>      administratively configured and which were obtained via other
>      mechanisms such as routing protocols.

**Status Update**:
: This requirement was taken into account when
       designing IETF solutions. Specifically, datastores are a fundamental
       concept in NETCONF/YANG (e.g., {{?RFC8342}}.

>      It is required to be able to fetch separately configuration data,
>      operational state data, and statistics from devices, and to be
>      able to compare these between devices.

**Status Update**:
: This is supported by NETCONF and RESTCONF.

>      It is necessary to enable operators to concentrate on the
>      configuration of the network as a whole rather than individual
>      devices.

**Status Update**:
: Protocols such as NETCONF supports means to
       handle transactions at the level of a network. For example, a
       controller can establish parallel sessions with a set of devices
       and make use of confirmed commit.
: Also, {{?RFC8969}} describes
       how YANG/RESTONF/YANG can be used to manage a network and map it
       to involves underlying functions/nodes. Several service and network
       data models are required for this aim.
: The IETF defined in the past
       models to manage few servcies such as VPN at both service and network
       levels (e.g.,  the Layer 2 Service Model (L2SM) {{?RFC8466}},
       the Layer 3 Service Model (L3SM) {{?RFC8299}}, the Layer 2 Network Model (L2NM) {{?RFC9291}},
       and the Layer 3 Network Model (L3NM) {{?RFC9182}}).
: A similar effort is currently
       ongoing for handling attachement circuits at both service and network layers (e.g.,
       {{?I-D.ietf-opsawg-teas-attachment-circuit}}, {{?I-D.ietf-opsawg-ntw-attachment-circuit}}).
: More effort is still needed in this area.

>      Support for configuration transactions across a number of devices
>      would significantly simplify network configuration management.

**Status Update**:
: This feature is supported by NETCONF.

>      Given configuration A and configuration B, it should be possible
>      to generate the operations necessary to get from A to B with
>      minimal state changes and effects on network and systems.  It is
>      important to minimize the impact caused by configuration changes.

**Status Update**:
: This feature is supported by NETCONF.

>      A mechanism to dump and restore configurations is a primitive
>      operation needed by operators.  Standards for pulling and pushing
>      configurations from/to devices are desirable.

**Status Update**:
: This feature is supported by NETCONF.

>      It must be easy to do consistency checks of configurations over
>      time and between the ends of a link in order to determine the
>      changes between two configurations and whether those
>      configurations are consistent.

**Status Update**:
: A mechanism is specified in {{?RFC9144}}.

>      Network wide configurations are typically stored in central
>      master databases and transformed into formats that can be pushed
>      to devices, either by generating sequences of CLI commands or
>      complete configuration files that are pushed to devices.  There
>      is no common database schema for network configuration, although
>      the models used by various operators are probably very similar.
>      It is desirable to extract, document, and standardize the common
>      parts of these network wide configuration database schemas.

**Status Update**:
: Covered by current implementations.

>      It is highly desirable that text processing tools such as diff,
>      and version management tools such as RCS or CVS, can be used to
>      process configurations, which implies that devices should not
>      arbitrarily reorder data such as access control lists.

**Status Update**:
: This is deployment-specific.

>      The granularity of access control needed on management interfaces
>      needs to match operational needs.  Typical requirements are a
>      role-based access control model and the principle of least
>      privilege, where a user can be given only the minimum access
>      necessary to perform a required task.

**Status Update**:
: RBAC is supported by existing implementation. Also,
       the IETF defined {{?RFC8341}} for this purpose.

>      It must be possible to do consistency checks of access control
>      lists across devices.

**Status Update**:
: This is implementation-specific.

>      It is important to distinguish between the distribution of
>      configurations and the activation of a certain configuration.
>      Devices should be able to hold multiple configurations.

**Status Update**:
: This is supported by existing NETCONF methods.

>      SNMP access control is data-oriented, while CLI access control is
>      usually command (task) oriented.  Depending on the management
>      function, sometimes data-oriented or task-oriented access control
>      makes more sense.  As such, it is a requirement to support both
>      data-oriented and task-oriented access control.

**Status Update**:
: This is supported by {{?RFC8341}}.
