# Earlier movement checklist

Historical planning reference. This document does not describe completed features or the current project backlog.

---

### Core Movement Features

#### 1. **Basic Movement**
- [ ] Implement `handle_movement_input()` to capture movement input (keyboard/controller) and process direction.
- [ ] Create `calculate_momentum(delta)` for smooth acceleration and deceleration based on input and current velocity.
- [ ] Add `apply_friction(delta)` to naturally slow down the player when no input is provided.

#### 2. **Stamina System**
- [ ] Add stamina-related variables:
  - [ ] `maxStamina` (default value, e.g., 100).
  - [ ] `currentStamina` (starts at `maxStamina`).
  - [ ] `staminaRecoveryRate` (default value, e.g., 5 per second).
- [ ] Implement `consume_stamina(amount)` to reduce stamina for actions like sprinting, dodging, etc.
- [ ] Add `recover_stamina(delta)` to regenerate stamina over time when not performing stamina-intensive actions.
- [ ] Create `has_sufficient_stamina(amount)` to check if stamina is enough for the requested action.

#### 3. **Momentum-Based Movement**
- [ ] Create `update_velocity(delta)` to adjust player velocity based on momentum and input direction.
- [ ] Add `apply_acceleration(input_direction, delta)` to increase velocity toward the input direction over time.
- [ ] Implement `handle_movement_chaining()` to support seamless transitions between actions like running, jumping, climbing, and landing.

---

### Advanced Movement Features

#### 4. **Sprinting**
- [ ] Implement `start_sprint()` to increase movement speed and begin consuming stamina.
- [ ] Add `stop_sprint()` to halt sprinting when stamina is depleted or the sprint button is released.

#### 5. **Dodging**
- [ ] Implement `perform_dodge(direction)` to execute quick evasive maneuvers in a given direction, temporarily boosting momentum and consuming stamina.
- [ ] Add `dodge_cooldown()` to enforce a cooldown period to prevent dodge spamming.

#### 6. **Jumping**
- [ ] Create `jump()` to launch the player upward, consuming stamina.
- [ ] Add `apply_jump_physics(delta)` to manage upward momentum during the jump and gravity pull during descent.

#### 7. **Climbing**
- [ ] Implement `check_climbable_surface()` to detect if the player can climb a surface.
- [ ] Add `start_climb()` to transition the player into a climbing state.
- [ ] Create `update_climb(delta)` to handle climbing movement and stamina consumption.
- [ ] Add `stop_climb()` to transition the player back to the ground or the top of the climbable surface.

#### 8. **Momentum-Based Movement Chaining**
- [ ] Implement `chain_movement(delta)` to handle fluid transitions between movement states like sprint → jump → climb → dodge.
- [ ] Add `calculate_action_momentum()` to adjust velocity and bonus momentum for chained actions.

---

### Physics and Smoothing

#### 9. **Gravity and Falling**
- [ ] Implement `apply_gravity(delta)` to apply downward force to the player when airborne.
- [ ] Add `check_grounded()` to determine if the player is on the ground.
- [ ] Create `land()` to reset momentum and trigger stamina recovery after landing.

#### 10. **Smoothing and Lag**
- [ ] Implement `lerp_velocity(target_velocity, current_velocity, smoothing)` for smooth velocity transitions.
- [ ] Add `lerp_rotation(target_rotation, current_rotation, smoothing)` for smooth directional adjustments.

---

### Input Handling

#### 11. **Directional Input**
- [ ] Create `get_camera_relative_input()` to convert player input into a world-space direction based on the camera's orientation.
- [ ] Implement `rotate_player_towards(direction)` for smooth rotation toward the movement direction.

---

### Environmental Interactions

#### 12. **Slope Handling**
- [ ] Implement `check_surface_angle()` to calculate the angle of the surface beneath the player.
- [ ] Add `apply_slope_physics(delta)` to adjust player movement and velocity when traversing slopes.

---

### Key Variables Setup
- [ ] Define movement-related variables:
  - [ ] `maxSpeed` (default, e.g., 6 units/second).
  - [ ] `acceleration` (default, e.g., 4 units/second²).
  - [ ] `deceleration` (default, e.g., 5 units/second²).
  - [ ] `momentum` (starts at 0).
- [ ] Define stamina-related variables:
  - [ ] `currentStamina`, `maxStamina`, `staminaRecoveryRate`.
- [ ] Define environmental variables:
  - [ ] `gravity` (default, e.g., -9.8 units/second²).
  - [ ] `groundFriction` (default, e.g., 0.8).
  - [ ] `slopeLimit` (default, e.g., 45 degrees).
