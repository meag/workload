# Weaponscripts

### Server-side weaponscripting

Remaining situation:
- forgetorder on, weapon 7 2 1
- keep firing as you run out of rockets, (1), pickup rockets, fire again (2)
  - (1) if you stop before firing shotgun, weaponlist should remain 7 2 1 and result (2) should be firing rocket
  - (1) if you continue and fire shotgun, weaponlist should change to 2 1, and result (2) should be firing shotgun
- issue is that ktx doesn't know about forgetorder and mvdsv doesn't know about ktx selecting best weapon from w_rank userinfo

### client-side rollover

- ezQuake has built-in 2-key rollover, but this only works if command is executed directly from keypress, not from alias from keypress
- would creating `/cl_weapon_rollover 1` (or `/weapon_r` & `+fire_r`) commands that have a 32-key rollover memory help people stop binding aliases to scripts?
- good example from ciscon's config, where releasing a key only fires -attack if it was the last key released
- Milton's qw non-blocking script [here](https://pastebin.com/YNfsvEcY)
