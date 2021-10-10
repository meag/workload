if it's on this list it's not released yet...

# ezQuake

### HDR

- [x] HDR mode should enable HDR lightmaps
- [x] Tonemap options - basic
- [x] Tonemap options - user configurable whitepoint
- [ ] Tonemap options - calculate from image (slower)
- [x] Restrict to certain rulesets, or are backgrounds just as bright as drawflat with wallcolor 255 255 255?  (same)
- [ ] remove immediate-mode bloom, glsl bloom

### Demo playback

- [ ] .avi/mjpeg output support in linux (done?  working on Windows, need to test)
- [ ] .mp4 support in windows, Visual Studio build only?  code is in another branch
- [x] fast demo rewind as long as within map reload time
- [ ] proper rewind (cl_demospeed -0.5) ... started on this but lot of work to make particles rewind etc

### Rendering

- [x] Translucent models should have a z-only pass to stop overdraw making the model more opaque
- [ ] Aliasmodel lerping is often janky
- [ ] OpenGL 3.2 support for MacOS in particular
- [ ] Fog
- [ ] 'Shadows'.... ugh.  remove old model
- [ ] long term
  - [ ] Integrate two particle systems, optimise
  - [ ] Common model format, get rid of lerphack
  - [ ] Proper md3 shader options
  - [ ] hud revamp, kill old hud & duplication of code
  - [ ] break link between console size and view limits/fov (lots of complaining)
  - [ ] r_gpu_particles/r_gpu_lighting etc - do vulkan first
- [ ] Vulkan
  - [ ] This is further forward but a slog at the moment until all the scaffolding is done
  - [x] Re-write brushmodel rendering to get rid of gpu_shader5 stuff that is now disabled
  - [ ] Multiple lightmap contexts, one context per texture (only worldmodels updated)
  - [ ] Support bindless texture extension & use that when rendering brushmodels instead

### Server browser/interface re-write

- [x] Threading model fixed (last corruption potentially fixed?)
- [x] Menu definitions read from .json files
- [x] Tabbed pages can take keyboard/input focus
- [ ] Better pages for showing explosion effects as options change
- [ ] Cancellable dialogs
- [ ] Load from badplace.json as a source (sources to have full servers, not just ip addresses)
- [ ] Grid view for server browser

# KTX

### Clan Arena - port ProX across

- [x] Go through Electro's ProX source-code and work out differences to core QW mod
- [ ] Fix spectating when dead (replace existing, possibly port)
- [ ] Support draw
  - [ ] match ends 0.5s after player is killed
  - [ ] match ends 4s after rocket launcher fired
  - [ ] match ends 5.5s after grenade launcher fired
  - [ ] match ends 3s after nailgun fired
- [ ] maps/platforms etc
  - [ ] Move hard-coded map support to .ent files
  - [ ] Sudden death support: spawn points, rules etc
  - [ ] push triggers can have target set (movedir calculated to hit targ entity at top of jump)
  - [ ] home_state/home_origin on spawn for platforms (dm2 discussion recently?)
  - [ ] dm6 door lg bug is dm6-only
  - [ ] map specific ents for SD spawns
  - [ ] precache shambler.mdl (?)
- [ ] combat
  - [ ] grenades have direct hit 110 damage
  - [ ] grenades don't explode on teammates
  - [ ] Rocket jump modifiers increase knockback on self-damage from rocket blast
  - [ ] x-ray damage option (radiusdamage doesn't look for line of sight)
  - [ ] can turn off falling damage
- [ ] audio
  - [ ] precache arena sounds
  - [ ] hitsounds based on damage done
  - [ ] new jump pad sound
  - [ ] taunt sounds?
  - [ ] convince dracs to re-record audio for countdown etc...
  - [ ] 5 minute warnings and 1 minute warnings
  - [ ] sounds == 2 platforms played quieter, default to sounds = 1 if not [1,2]
  - [ ] cust_sound1/cust_sound2 over-rides self.sounds
  - [ ] different sound for jump pads
- [ ] misc others
  - [ ] there is a bigger list
  - [ ] menus (lower priority)
  - [ ] multiple arenas (lower priority)

### Weaponscripts

- [ ] Give up on mvdsv setting this, KTX changes weapons under too many circumstances
- [ ] mvdsv should just convert to a usercmd and let ktx pick up parameters
- [ ] forgetorder :/

### Race mode

- [ ] Concurrent multi-racing (requires mvdsv recording 33 concurrent demos...) - in progress
- [ ] Replace pacemaker with bots replaying user's commands - in progress

### Networking improvements

- [ ] maybe just park this until andeh's stuff done

# Demolyzer (html)

- [ ] Version 1
  - [ ] Load map images from server if available (github repo)
  - [ ] Non-html screenshots
  - [ ] Github repo for static content
  - [ ] Graphs based on original program
  - [ ] Table results based on original program
- [ ] Longer term
  - [ ] Multi-map matches
  - [ ] Submit to tournament websites
  - [ ] Integration with gfx.quakeworld.nu

# Badplace

- [ ] Fix race records where route numbers have been mis-identified
- [ ] Get to the bottom of this
- [ ] Accept match results from Demolyzer
- [ ] Enable tournament admin accounts (GQ5)
- [ ] Update wiki sync for changes to templates (GQ5)
- [ ] Show wiki sync status on-screen to admins
- [ ] Parse api data from dev's old site
- [ ] Upload old GetQuad demos and associate with tournament games
