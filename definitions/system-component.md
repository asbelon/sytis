---
title: Компонент системы
description: 
published: false
date: 2025-06-19T18:37:07.952Z
tags: term
editor: markdown
dateCreated: 2025-06-19T18:29:18.639Z
---

> Компонент - часть системы, вступающая в определенные отношения с другими частями (подсистемами, компонентами, элементами)
{.is-info}

```plantuml
@startuml

skinparam monochrome true
skinparam linetype ortho

entity "Классификатор" as Classifier {
	id : integer
	external_id : string[uuid]
	code : string
	name : string
}

entity "Система" as System {}

entity "Компонент" as Component {
	description : text
	system : System
}
Component -up-|> Classifier
System o-r- Component

@enduml
```