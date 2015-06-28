== empty-project
:idprefix: id_ 
(choose one, do not modify, then add a second sentence with a brief description, starting with - "The empty-project addon enables blah blah...)
This addon provides *standalone* functionality, and *exports services* for use in other addons. 
This addon provides *standalone* functionality.
This addon *exports services* for use in other addons. 
This addon *provides classes* for use in other addons. 
This addon is a 'Furnace container' that provides *lifecycle* and *service registry* support for dependent addons.
        
=== Dependencies: None (or)
=== Depends on
[options="header"]
|===
|Addon |Exported |Optional
|DEP1
|yes
|no
|DEP2
|yes
|yes
|===

== Setup

This Addon requires the following installation steps.

=== Add configuration to pom.xml 

To use this addon, you must add it as a dependency in the *pom.xml* of your `forge-addon` classified artifact:
(Make sure the dependency is put all the way to the left, and uses 3 spaces for indentation of GAV)
[source,xml]
----
<dependency>
   <groupId>unknown</groupId>
   <artifactId>empty-project</artifactId>
   <classifier>forge-addon</classifier>
   <version>${version}</version>
</dependency>
----
== Features
ABCFactory for simple ABC blah:: 
Allows for blah blah
+
[source,java]
----
@Inject private ABCFactory factory;
ABC abc = factory.createABC();
----
+
[TIP] 
====
If your addon uses a container that does not support "@Inject" annotations, services such as the `ABCFactory` may also be 
accessed via the `AddonRegistry`:
----
Imported<ABCFactory> imported = addonRegistry.getServices(ABCFactory.class);
ABCFactory factory = imported.get();
----
==== 
Creating a new XYZ instance:: 
Causes XYZ to occur
+
[source,java]
----
XYZ xyz = factory.createXYZ();
----
