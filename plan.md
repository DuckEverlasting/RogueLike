class Floor:
  - level *

class Tile:
  - floor *
  - coord *
  - occupant
  - terrain
  - explored
  - items

class Object:
  - id *

class Mob:
  - id *
  - attitude
  - behavior
  - hp
  - ac
  - speed
  - xp
  - drops


class Player:
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
  - body
  - mainHand
  - offHand
  - necklace
  - ringA
  - ringB
  - inv
  - spells

class Item:
  - id *
  - autoPickup
  - weight

  subclass Gold:
    - amount

  subclass Consumable:
    - onUse

  subclass Missile:
    - amount
    - weaponType
    - weaponRequired

  subclass Wearable:
    - cursed
    - armor
    - effects

    subclass Handheld:
      - twoHanded
      - offHand
      - ranged