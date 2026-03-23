# Dark Fantasy Game - Gameplay Guide

## Quick Start

1. Open `DarkFantasyGame.html` in any modern web browser
2. Use **arrow keys** or **WASD** to move
3. Attack enemies by walking into them
4. Collect substances to gain buffs
5. Use **Spacebar** to dash, **E** for cleave, **H** to heal
6. Survive 10 kills per level to progress
7. Try to reach the highest level possible!

## Game Mechanics

### Combat System
- **Auto-attack**: Walk into enemies to attack (0.5s cooldown)
- **Damage calculation**: Base 10 × buff multipliers × enemy proximity
- **Knockback**: Successful hits push enemies away
- **Hit feedback**: Orange particles on successful hits
- **Enemy counters**: Enemies push back when they hit you

### Buff System (Original 5 Substances)
Apply by pressing **1-5** or clicking inventory slots

| Substance | Effect | Duration | Loot From |
|-----------|--------|----------|-----------|
| 🍺 Beer | 1.2× Damage | 30s | Zombie, Golem |
| 💨 Cigarettes | 1.15× Speed | 40s | Knight, Plague Warden |
| 🥃 Shots | +10 HP Heal | 25s | Zombie, Assassin |
| 📦 Snus | 1.15× Defense | 35s | Knight, Golem |
| ⚪ Line | 1.4× Damage + 1.25× Speed | 20s | Wraith, Assassin |

### Leveling System
- **Level up every 10 kills** (per level)
- **Progression example**:
  - Level 1: 10 kills to level 2
  - Level 2: 10 kills to level 3
  - Level 3: 10 kills to level 4
  - etc.
- **Each level**:
  - +10 max HP
  - +20% enemy HP (scaled)
  - +20% enemy damage (scaled)
  - New dungeon generation
  - More enemy spawns (3 + level count)

### Enemy Types

| Enemy | HP | Dmg | Speed | Notes |
|-------|----|----|-------|-------|
| 🧟 Zombie | 30 | 5 | 1.0 | Balanced, common |
| ⚔️ Knight | 25 | 8 | 1.5 | Medium threat |
| 👻 Wraith | 15 | 10 | 2.0 | Fast, high damage |
| 🗿 Golem | 50 | 3 | 0.5 | Tanky, slow |
| 🥷 Assassin | 10 | 12 | 3.0 | Deadly glass cannon |
| 🦠 Warden | 20 | 6 | 1.2 | Ranged threat |

*Stats scale by 1 + (Level-1) × 0.2 for levels 2+*

### Special Abilities

#### Dash (SPACE) - Cooldown: 3 seconds
- Quick 40-pixel teleport in your facing direction
- Creates green particles
- Perfect for dodging incoming attacks
- No damage immunity (be careful!)

#### Cleave (E) - Cooldown: 5 seconds
- AoE attack in 100-pixel radius
- 1.5× your normal damage to all enemies hit
- Knocks back all targets
- Creates red particles and screen shake
- Great for crowds

#### Heal (H) - Cooldown: 15 seconds
- Restore 30 HP (caps at max)
- Only works if you're below max HP
- Creates healing particles
- Essential for survival

## Scoring System

- **Base**: 20 points per kill
- **Scaling**: Multiplied by (1 + (Level-1) × 0.5)
  - Level 1: 20 points per kill
  - Level 2: 30 points per kill
  - Level 3: 40 points per kill
  - etc.
- **Final Score**: Displayed on game over

## Game Over & Leaderboard

When you die:
1. Screen shows "DEFEATED"
2. Statistics displayed:
   - Final level
   - Kills
   - Score
   - Time survived
3. Prompted to enter name for leaderboard
4. Top 10 scores saved locally
5. Click "RESTART GAME" to play again

## Advanced Strategy

### Early Game (Levels 1-2)
- Focus on collecting substances
- Build up buffs before fighting harder enemies
- Use Line substance for burst damage when needed
- Dodge Assassins (one shot threat)

### Mid Game (Levels 3-5)
- Mix Cleave ability usage with dodging
- Use Dash to kite Wraiths
- Group kiting (pull enemies and cleave)
- Maintain buffs for damage

### Late Game (Level 6+)
- Spam Cleave for AoE dominance
- Use Dash for positioning
- Heal frequently (15s CD)
- Focus on score multiplier stacking

### Enemy-Specific Tips
- **Zombie**: Low threat, farm for loot
- **Knight**: Moderate threat, cleave when grouped
- **Wraith**: High threat, use Dash to escape
- **Golem**: Tanky but slow, just dash past
- **Assassin**: DEADLY! Avoid 1v1, use Cleave/Heal
- **Warden**: Ranged attacker, dash sideways

## Control Summary

### Keyboard
- **Arrow Keys / WASD**: Movement
- **1-5**: Use Substance (Beer, Cigs, Shots, Snus, Line)
- **SPACE**: Dash Ability
- **E**: Cleave Ability (AoE)
- **H**: Heal Ability

### Mouse
- **Click substance slots**: Use items

### Mobile
- **D-Pad buttons**: Movement
- **Substance buttons**: Touch to use
- **Note**: Abilities require keyboard (future update)

## HUD Explanation

### Top-Left (Status)
- **HP**: Current health / Max health
- **Kills**: Current kills / Target kills to level
- **Time**: Elapsed time in game
- **Level**: Current level number
- **Score**: Total score accumulated
- **Buffs**: Active buff list with duration

### Bottom-Left (Inventory)
- **5 substance slots** showing count
- **Click to use** substances
- Hover for interaction feedback

### Bottom-Right (Abilities)
- **3 ability items** showing status
- **Greyed out** when on cooldown
- **Shows cooldown time** remaining

## Persisted Data

### Auto-Save
- Game state saved on death
- Includes: Level, HP, Score, Inventory
- Used for stats display

### Leaderboard
- Top 10 scores stored locally
- Includes: Name, Score, Date
- Persistent across browser sessions

## Tips & Tricks

1. **Substance Stacking**: Stack similar buffs by using before they expire
2. **Cleave Timing**: Use Cleave when enemies are grouped
3. **Dash Escape**: Dash away from Assassins immediately
4. **Heal Efficiency**: Save Heal for critical moments (20%+ damage taken)
5. **Loot Farming**: Zombies and Golems drop best early loot
6. **Level Speed**: Rushing levels increases difficulty - balance carefully
7. **Score Optimization**: Higher levels = better points per kill
8. **Multi-buff**: Apply multiple buffs for multiplicative effect
9. **Defense Stacking**: Snus buff reduces damage taken
10. **Knockback Usage**: Use enemy knockback to create space

## Troubleshooting

### Game Won't Start
- Refresh the page
- Check console for errors (F12)
- Ensure JavaScript is enabled

### Leaderboard Empty
- Check browser allows localStorage
- Private browsing mode disables storage
- Clear storage: DevTools → Application → Storage → Clear All

### Performance Issues
- Reduce particle count by avoiding abilities
- Close other browser tabs
- Try different browser
- Lower-end devices may lag at Level 5+

### Controls Not Working
- Check NumLock (if using numeric arrows)
- Mobile users: Use on-screen D-pad
- Try keyboard in different browser
- Check for full-screen exclusivity

## Achievements (Unofficial Goals)

Try to achieve these milestones:

- **Speed Killer**: Beat level 1 in under 30 seconds
- **Survivor**: Reach level 5
- **Master**: Reach level 10
- **Perfect Run**: Beat level 1 with full HP
- **Leaderboard**: Get top 3 on leaderboard
- **Cleave Master**: Kill 10 enemies with Cleave
- **Last Stand**: Score 1000+ points
- **Max Level**: Reach level 20

---

**Good luck, adventurer! May your blows be strong and your substances plentiful.**
