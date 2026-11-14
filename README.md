HELLO EVERYONE,
Let me brief you on how the game works.

The game is a loop. You plan a sol, press “End sol”, the game works out what happened, and the screen redraws.

Your turn

Each sol you have 4 crew-hours to spend with the + and − buttons. Building something (solar, oxygen plant, greenhouse, shielding) raises its level by 1 per crew-hour, up to level 8. Science gives 10 points per crew-hour, and rest heals 4 health per crew-hour. You have to spend all 4 before you can end the sol.

What happens when you end the sol

The game resolves things in this order:

Power. Panels make solar level × 4 × sunlight. Demand is 4 + oxygen level × 1.5 + greenhouse level × 2. Any surplus charges the battery (max 100). If the battery plus panel output can’t cover demand, the battery drops to zero and the oxygen plant and greenhouse run at a reduced percentage. That’s a brownout.
Life support. Oxygen changes by plant level × 3 × power ratio − 4, because the crew breathes 4 per sol. Food works the same way with the greenhouse. Both are capped at 0–100.
Radiation. Daily dose is max(0, site radiation − shield level × 1.2). A solar flare adds max(0, flare strength − shield level × 2.2). Crew health drops by 0.6 per unit of dose. On the Moon, shield level 5 cancels the daily dose entirely.
Emergencies. If oxygen hits 0, health drops 25. If food hits 0, it drops 12. A meteor shower knocks one random system (solar, oxygen, or greenhouse) down a level.
Win or lose. Health at 0 ends the mission. Surviving sol 30 wins, with score science + health × 2 + (oxygen + food) ÷ 2.

Why the choices feel hard

At the start, oxygen and food production are slightly below what 4 crew need, so you can’t just coast.
Upgrading oxygen or the greenhouse raises power demand, so you also need panels.
On the Moon, the short blackout nights cut panel output to 10%, so you need a charged battery. On Mars, sunlight is always weak and dust storms cut it further.
Shielding does nothing visible until a flare or a long stretch of radiation, so it’s tempting to skip. Science feels rewarding but doesn’t keep anyone alive.

Developed by adi-unfazed with Super Intelligence (SI) assistance for code generation, UI styling, and interactive layout.
