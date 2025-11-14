Game Concept: The Character Abilities Showcase

This project brings to life a small combat system where classic RPG archetypes fight, cast spells, heal allies, and show off their strengths through clean inheritance and polymorphism.
You get to choose from four unique heroes: the powerful Warrior (Ariah), the mystical Mage (Memphis), the swift Rogue (Lyra), and the holy Cleric (Elara).
Each class has its own fighting style, special abilities, and magic aptitude, and the system reliably demonstrates their differences using object-oriented programming principles.

Design Choices: Class Structure & Abilities

The goal was to make each class feel distinct while still sharing a common foundation.
To achieve this, I used a clean inheritance hierarchy:

Character  →  Player  →  (Warrior, Mage, Rogue, Cleric)


The base Character class handles universal stats and behaviors like HP, strength, magic, basic attacking, and damage calculation.
The Player class builds on this by adding RPG-specific features such as level, experience, and class titles.

Each subclass then overrides the attack() method and adds its own signature move:

Warrior (Ariah)

A powerhouse with high HP (120) and massive Strength (15).
Their attack() adds bonus physical damage, and their Power Strike deals double Strength damage for heavy hits.

Mage (Memphis)

High Magic (20), low Strength — the definition of a glass cannon.
Their attack() uses magic instead of strength, and Fireball unleashes destructive magical damage equal to double their Magic stat.

Rogue (Lyra)

Agile and clever with balanced stats.
Their quick-strike attack() does extra light damage, and Sneak Attack guarantees a critical hit worth triple their Strength.

Cleric (Elara)

A supportive spellcaster with strong Magic (15) and good Health (110).
Their attack() fuses magic into melee, and they can cast Heal, restoring huge amounts of HP to allies.

This entire system cleanly demonstrates polymorphism:
all characters use the method attack(), yet they all behave differently!

BONUS Creative Feature: Weapon Composition

I added a Weapon class to demonstrate composition (a HAS-A relationship).
Characters don’t inherit from weapons — they carry them.

Each weapon has:

a name

a damage bonus

Weapons are displayed through a simple display_info() method, and the main program shows how characters can equip different gear like:

Aetherium Greatsword

Prism Staff of Mana

Twin Shadow Blades

This adds personality to each class’s fighting style and shows how composition works in object-oriented design.

AI Code Stuff

I used AI mainly for debugging issues, such as:

fixing inheritance mistakes

repairing attack logic

catching typos in overridden methods

ensuring the battle loop ran cleanly

validating polymorphism behavior

AI helped me with debugging issues, such as calling out indention problems

How to Run My Code

To run and verify the entire showcase, follow these steps:

Navigate to the Project Directory

Open your terminal and move into the folder where your file is located:

cd project-2-CharacterShowcase

Run the Program

Execute the Python file to generate all characters, display their stats, test polymorphism, show special abilities, demonstrate weapons, and run the battle simulation:

python project2.py


You will see:

stats for all four classes

their unique attack methods

their special abilities

weapon information

a full battle: Warrior vs Mage

## 🎨 Bonus Creative Elements

Feel free to add your own creative touches for bonus points:
- Additional character classes beyond the three required
- More weapon types with different properties
- Enhanced special abilities with unique effects
