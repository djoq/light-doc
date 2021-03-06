---
title: "Graphql Router"
date: 2017-11-29T21:00:16-05:00
description: ""
categories: []
keywords: []
slug: ""
aliases: []
toc: false
draft: false
---

Graphql Router is responsible for handling GraphQL and GraphiQL requests and hooks schema provider.
It provides RouteHandler and SchemaProvider interfaces and implement both GET and POST handlers 
for GraphQL.

The router is a HandlerProvider and it needs to be put into service.yml config file.

This [link][] is an example.

The user developed schema needs to be hooked to the GraphqlPostHandler in this module through 
SchemaProvider interface. The service.yml config file should include the implementation of the
com.networknt.graphql.router.SchemaProvider

Another [example][].

[link]: https://github.com/networknt/light-example-4j/blob/master/graphql/mutation/src/main/resources/META-INF/services/com.networknt.server.HandlerProvider
[example]: https://github.com/networknt/light-example-4j/blob/master/graphql/mutation/src/main/resources/META-INF/services/com.networknt.graphql.router.SchemaProvider
