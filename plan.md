class Floor:
  - level *
  - type

class Room:
  - id *
  - floor *
  - name
  - desc
  - type
  - visited

class Tile:
  - floor *
  - room *
  - coord *
  - sprite
  - occupant
  - terrain
  - visited
  - items

class Object:
  - id *
  - type
  - sprite
  - passable
  - approachBehavior()

class Mob:
  - id *
  - type
  - sprite
  - hp
  - ac
  - speed
  - xp
  - attitude
  - drops
  - mobBehavior()

class Player(Singleton):
  - sprite
  - class
  - race
  - str
  - dex
  - int
  - con
  - perception
  - level
  - xp
  - hp
  - mp
  - status
  - loc
  - head
  - body
  - legs
  - mainHand
  - offHand
  - neck
  - fingerA
  - fingerB
  - inv
  - spells
  - move()
  - equip()
  - unequip()
  - use()
  - cast()
  - attack()
  - throw()
  - look()
  - get()
  - drop()
  - wait()

class Item:
  - id *
  - sprite
  - autoPickup
  - weight

  subclass Gold:
    - amount

  subclass Consumable:
    - type
    - onUse()

  subclass Missile:
    - amount
    - weaponType
    - weaponRequired
    - damage

  subclass Wearable:
    - type
    - cursed
    - armor
    - effects

    subclass Handheld:
      - twoHanded
      - offHand
      - ranged
      - damage