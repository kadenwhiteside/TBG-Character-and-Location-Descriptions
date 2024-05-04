# TBG-Character-and-Location-Descriptions


This code goes over the characters, their inventories, and the locations in the game that I created but I haven't coded yet. 


# TBG Nested Dictionaries - Kaden Whiteside
# April 27, 2024


# This code utilizes nested dictionaries for organizational purposes
# This code will print out the characters, their invenories, and locations
# Basically all basis' of the game will be covered

# Note that I don't think using indevidual functions for this code is the-
# -way to go about doing this task, I will be foregoing functions along with-
# -the doumentation that follows each function.


# Nested dictionaries for the characters, locations, and their inventories
game_data = {
    "characters": {
        "You": {
            "description": "You are the protagonist, the main character, the vessel that sees this made up world. You are nameless. You have a dog that you must find.",
            "inventory": {
                "food": {
                    "bread with honey butter": {
                        "description": "A delicious snack to keep you energized."
                    },
                    "water": {
                        "description": "Essential for staying hydrated during your journey."
                    },
                    "steak": {
                        "description": "A hearty meal to satisfy your hunger."
                    },
                    "baked potato": {
                        "description": "A filling and comforting food option."
                    }
                },
                "utilities": {
                    "flashlight": {
                        "description": "A handy tool to illuminate dark areas."
                    },
                    "hiking shoes": {
                        "description": "Sturdy shoes that provide a 10% boost in hiking speed."
                    },
                    "sneakers": {
                        "description": "Lightweight shoes that make you 10% sneakier."
                    }
                },
                "pants": {
                    "jeans": {
                        "description": "Durable and comfortable jeans for everyday wear."
                    },
                    "joggers": {
                        "description": "Comfortable pants suitable for light exercise or leisure."
                    },
                    "sweatpants": {
                        "description": "Casual and cozy pants perfect for lounging."
                    }
                }
            }
        },
        "Dog": {
            "description": "This is the dog belonging to the user, they know to stay on trails, however they do get lost from time to time.",
            "inventory": {
                "collar with nametag": {
                    "description": "A collar with a nametag containing the owner's phone number and address."
                }
            }
        },
        "Bungus the Lion": {
            "description": "Bungus lives in the forest. They are a friendly lion, they love helping others whenever they can. They know about the whereabouts of most creatures in the forest."
        },
        "Marrr the Tiger": {
            "description": "Marrr is a creature of the forest, she is mean, she don't like others being in her space. Marrr also loves to play games, she will always pick the same option in a game too."
        },
        "Bear": {
            "description": "The bear is protective of his area, they don't like other creatures either. Overall the Bear likes to be left alone... hopefully you don't have to interact with them at all.",
            "inventory": {
                "honey": {
                    "description": "The most sacred posession of the Bear."
                }
            }
        }
    },
    "locations": {
        "Campsite": {
            "description": "This is the home of You and your Dog, it is a safe space where all of your items are stored too."
        },
        "Tent": {
            "description": "This is your place of rest, sleeping and relaxing are done in here. Other than that the tent is used for nothing else."
        },
        "Safe but dark trail": {
            "description": "The desription is in the name, it is a longer path to the Bear den but it is safer, however it is much spookier. This is the area that Marrr lives as she likes the darkness."
        },
        "Dangerous and well lit trail": {
            "description": "THe description is in the name. This is a short path to the bear den. However it is a very dangerous and steep path, difficult to climb. This is the area that Bungus lives as well."
        },
        "Bear den": {
            "description": "Home of the Bear. All paths lead to here evenually (how does that even work? Doesn't matter, just trust the logic of this forest trail). The Bear den is sacred to the Bear so do not enter unless you absolutely have to."
        }
    }
}


# Printing out characters
print("Characters:\n")
for character, data in game_data["characters"].items():
    print(f"{character.capitalize()}: {data['description']}")
    if "inventory" in data:
        print("Inventory:")
        for category, items in data["inventory"].items():
            print(f"- {category.capitalize()}")
            for item, details in items.items():
                if isinstance(details, dict):
                    print(f"  - {item.capitalize()}: {details.get('description', 'No description')}")
    print()                                                                                             # Add new line after each character


# Printing out locations
print("Locations:\n")
for location, data in game_data["locations"].items():
    print(f"{location.capitalize()}: {data['description']}")
    print()                                                                                             # Add new line after each location



