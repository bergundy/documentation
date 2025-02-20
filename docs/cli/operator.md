---
id: operator
title: Temporal CLI operator command reference
sidebar_label: operator
description: How to use the Temporal CLI operator commands
toc_max_heading_level: 4
keywords:
- cli reference
- cluster
- cluster health
- cluster list
- cluster remove
- cluster upsert
- command-line-interface-cli
- describe
- namespace
- namespace create
- namespace delete
- namespace describe
- namespace list
- operator
- search attribute
- search attribute create
- search attribute list
- search attribute remove
- system
- temporal cli
- update
tags:
- cli-reference
- cluster
- cluster-health
- cluster-list
- cluster-remove
- cluster-upsert
- command-line-interface-cli
- describe
- namespace
- namespace-create
- namespace-delete
- namespace-describe
- namespace-list
- operator
- search-attribute
- search-attribute-create
- search-attribute-list
- search-attribute-remove
- system
- temporal-cli
- update
---

<!-- THIS FILE IS GENERATED. DO NOT EDIT THIS FILE DIRECTLY -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

Operator commands enable actions on [Namespaces](/namespaces#), [Search Attributes](/visibility#search-attribute), and [Temporal Clusters](/clusters#).
These actions are performed through subcommands.

To run an Operator command, run `temporal operator [command] [subcommand] [command options]`.

## cluster

Cluster commands enable actions on [Temporal Clusters](/clusters#).

Cluster commands follow this syntax:
`temporal operator [command] [subcommand] [command options]`.

### describe

The `temporal operator cluster describe` command shows information about the [Cluster](/clusters#).
This information can include information about other connected services, such as a remote [Codec Server](/dataconversion#codec-server).

Use the following options to change the output of this command.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--fields](/cli/cmd-options#fields)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--output](/cli/cmd-options#output)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### health

The `temporal operator cluster health` command checks the health of the [Frontend Service](/clusters#frontend-service).
A successful execution returns a list of [Cluster](/clusters#) metrics.

Use the following options to change the behavior and output of this command.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### list

The `temporal operator cluster list` command prints a list of all remote [Clusters](/clusters#) on the system.

`temporal operator cluster list`

Use the following options to change the command's behavior.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--fields](/cli/cmd-options#fields)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--limit](/cli/cmd-options#limit)

- [--namespace](/cli/cmd-options#namespace)

- [--no-pager](/cli/cmd-options#no-pager)

- [--output](/cli/cmd-options#output)

- [--pager](/cli/cmd-options#pager)

- [--time-format](/cli/cmd-options#time-format)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### remove

The `temporal operator cluster remove` command removes a remote [Cluster](/clusters#) from the system.

`temporal operator cluster remove --name=SomeCluster`

Use the following options to change the command's behavior.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--name](/cli/cmd-options#name)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### system

The `temporal operator cluster system` command provides information about the system the [Cluster](/clusters#) is running on.
This information can be used to diagnose problems occurring in the [Temporal Server](/clusters#temporal-server).

`temporal operator cluster system`

Use the following options to change this command's behavior.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--fields](/cli/cmd-options#fields)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--output](/cli/cmd-options#output)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### upsert

The `temporal operator cluster upsert` command allows the user to add or update a remote [Cluster](/clusters#).
`temporal operator cluster upsert --frontend-address="127.0.2.1"`

Upserting can also be used to enable or disabled cross-cluster connection.
`temporal operator cluster upsert --enable-connection=true`

Use the following options to change the behavior of this command.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--enable-connection](/cli/cmd-options#enable-connection)

- [--env](/cli/cmd-options#env)

- [--frontend-address](/cli/cmd-options#frontend-address)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

## namespace

Namespace commands perform operations on [Namespaces](/namespaces#) contained in the [Temporal Cluster](/clusters#).

Namespace commands follow this syntax:
`temporal operator namespace COMMAND [ARGS]`.

### create

The `temporal operator namespace create` command creates a new [Namespace](/namespaces#).
The Namespace can be created on the active [Cluster](/clusters#), or any named Cluster within the system.
`temporal operator namespace --cluster=MyCluster`

Global Namespaces can also be created.
`temporal operator namespace create --global`

Other settings, such as [retention](/clusters#retention-period) and [Visibility Archival State](/clusters#visibility), can be configured according to the application's needs.
The Visibility Archive can be set on a separate URI.
`temporal operator namespace create --retention=RetentionMyWorkflow --visibility-archival-state="enabled" --visibility-uri="some-uri"`

Use the options listed below to change the command's behavior.

- [--active-cluster](/cli/cmd-options#active-cluster)

- [--address](/cli/cmd-options#address)

- [--cluster](/cli/cmd-options#cluster)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--data](/cli/cmd-options#data)

- [--description](/cli/cmd-options#description)

- [--email](/cli/cmd-options#email)

- [--env](/cli/cmd-options#env)

- [--global](/cli/cmd-options#global)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--history-archival-state](/cli/cmd-options#history-archival-state)

- [--history-uri](/cli/cmd-options#history-uri)

- [--namespace](/cli/cmd-options#namespace)

- [--retention](/cli/cmd-options#retention)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

- [--visibility-archival-state](/cli/cmd-options#visibility-archival-state)

- [--visibility-uri](/cli/cmd-options#visibility-uri)

### delete

The `temporal operator namespace delete` command deletes a given [Namespace](/namespaces#) from the system.
The command follow the syntax `temporal operator namespace delete <namespace>`

Use the following options to change the behavior of this command.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

- [--yes](/cli/cmd-options#yes)

### describe

The `temporal operator namespace describe` command provides a description of a [Namespace](/namespaces#).
Namespaces are identified by Namespace ID.

`temporal operator namespace describe --namespace-id=meaningful-business-id`

Use the following options to change the behavior of this command.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--namespace-id](/cli/cmd-options#namespace-id)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### list

The `temporal operator namespace list` command lists all [Namespaces](/namespaces) on the [Server](/clusters#frontend-service).

`temporal operator namespace list`

Use the following options to change this command's behavior.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### update

The `temporal operator namespace update` command updates a [Namespace](/namespaces#).

Namespaces can be assigned a different active [Cluster](/clusters#).
`temporal operator namespace update --active-cluster=NewActiveCluster`

Namespaces can also be promoted to global Namespaces.
`temporal operator namespace --promote-global=true`

Any [Archives](/clusters#archival) that were previously enabled or disabled can be changed through this command.
However, URI values for archival states cannot be changed after the states are enabled.
`temporal operator namespace update --history-archival-state="enabled" --visibility-archival-state="disabled"`

Use the options listed below to change the command's behavior.

- [--active-cluster](/cli/cmd-options#active-cluster)

- [--address](/cli/cmd-options#address)

- [--cluster](/cli/cmd-options#cluster)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--data](/cli/cmd-options#data)

- [--description](/cli/cmd-options#description)

- [--email](/cli/cmd-options#email)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--history-archival-state](/cli/cmd-options#history-archival-state)

- [--history-uri](/cli/cmd-options#history-uri)

- [--namespace](/cli/cmd-options#namespace)

- [--promote-global](/cli/cmd-options#promote-global)

- [--retention](/cli/cmd-options#retention)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

- [--verbose](/cli/cmd-options#verbose)

- [--visibility-archival-state](/cli/cmd-options#visibility-archival-state)

- [--visibility-uri](/cli/cmd-options#visibility-uri)

## search-attribute

Search Attribute commands enable operations for the creation, listing, and removal of [Search Attributes](/visibility#search-attribute).

Search Attribute commands follow this syntax:
`temporal operator search-attribute COMMAND [ARGS]`.

### create

The `temporal operator search-attribute create` command adds one or more custom [Search Attributes](/visibility#search-attribute).
These Search Attributes can be used to [filter a list](/visibility#list-filter) of [Workflow Executions](/workflows#workflow-execution) that contain the given Search Attributes in their metadata.

Use the following options to change this command's behavior.

- [--fields](/cli/cmd-options#fields)
- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--name](/cli/cmd-options#name)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

- [--type](/cli/cmd-options#type)

### list

The `temporal operator search-attribute list` command displays a list of all [Search Attributes](/visibility#search-attribute) that can be used in [Queries](/workflows#query).

`temporal workflow list --query`.

Use the following options to change this command's behavior.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--namespace](/cli/cmd-options#namespace)

- [--output](/cli/cmd-options#output)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

### remove

The `temporal operator search-attribute remove` command removes custom [Search Attribute](/visibility#search-attribute) metadata.
This command does not remove custom Search Attributes from Elasticsearch or change the index schema.

Use the following options to change this command's behavior.

- [--address](/cli/cmd-options#address)

- [--codec-auth](/cli/cmd-options#codec-auth)

- [--codec-endpoint](/cli/cmd-options#codec-endpoint)

- [--color](/cli/cmd-options#color)

- [--context-timeout](/cli/cmd-options#context-timeout)

- [--env](/cli/cmd-options#env)

- [--grpc-meta](/cli/cmd-options#grpc-meta)

- [--name](/cli/cmd-options#name)

- [--namespace](/cli/cmd-options#namespace)

- [--tls](/cli/cmd-options#tls)

- [--tls-ca-path](/cli/cmd-options#tls-ca-path)

- [--tls-cert-path](/cli/cmd-options#tls-cert-path)

- [--tls-disable-host-verification](/cli/cmd-options#tls-disable-host-verification)

- [--tls-key-path](/cli/cmd-options#tls-key-path)

- [--tls-server-name](/cli/cmd-options#tls-server-name)

- [--yes](/cli/cmd-options#yes)

