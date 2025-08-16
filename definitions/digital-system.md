---
title: Цифровая система
description: 
published: false
date: 2025-06-18T16:54:42.041Z
tags: term
editor: markdown
dateCreated: 2025-06-18T16:34:16.439Z
---

> Цифровая система - это информационная система для вычислительной обработки цифровых данных. 
{.is-info}

Информационная система - это ФС, поэтому и цифровая система является функциональной.

Взаимодействие внешней среды с ФС происходит на её границе (интерфейса), следовательно каждая ЦС обладает интерфейсом или интерфейсами.

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

entity "Система" as System {
	description : text|null
	boundary : System|null
}
System -up-|> Classifier

entity "Интерфейс" as Interface {
	type : string[REST API|UI]
	specification : text[json|yaml]
}
Interface }|-l-|| System
    
@enduml
```