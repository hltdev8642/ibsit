# IBSIT v2.0 - Impact Based Structural Integrity Test

## Overview

Enhanced version of the Impact Based Structural Integrity Test mod for Teardown, featuring advanced structural simulation with realistic collapse mechanics, enhanced visuals, sounds, and performance optimizations.

## New Features (v2.0)

### 🎯 Enhanced Structural Simulation

- **Material-Specific Damage**: Different materials now have unique damage multipliers and behaviors
- **Advanced Shape Manipulation**: Uses new Teardown 1.4.0+ API functions for better structural integrity
- **Improved Physics**: More realistic momentum calculations and collapse patterns

### 🎨 Visual Enhancements

- **Enhanced Particles**: Material-specific particle effects with quality settings
- **Dynamic Lighting**: Emissive particles for metal impacts
- **Performance Monitoring**: Real-time stats display during gameplay

### 🔊 Audio & Haptics

- **Structural Sound Effects**: Different sounds for light/heavy collapses and stress
- **Haptic Feedback**: Controller vibration for impacts (requires compatible hardware)
- **Volume Control**: Adjustable sound levels

### ⚙️ Advanced Configuration

- **Particle Quality Settings**: Low/Medium/High quality options
- **Protection Mode**: Safeguard specific objects with tags
- **Vehicle & Joint Options**: Fine-tune what gets affected by structural integrity
- **Enhanced UI**: Modern interface with better organization

## Installation

1. Replace `main.lua` with `main_enhanced.lua`
2. Replace `options.lua` with `options_enhanced.lua`
3. Create the following folder structure:

   ```
   mods/ibsit/
   ├── sounds/
   │   ├── collapse_heavy.ogg
   │   ├── collapse_light.ogg
   │   └── structure_stress.ogg
   ├── haptic/
   │   ├── impact_light.xml
   │   └── impact_heavy.xml
   └── vox/
       └── (your custom models)
   ```

## Configuration Options

### Core Settings

- **Dust Amount**: Controls debris particle count (0-100)
- **Material Damage**: Separate multipliers for soft/medium/hard materials
- **Momentum Threshold**: Sensitivity of structural failure detection

### Feature Toggles

- **Enhanced Particles**: Improved visual effects
- **Sound Effects**: Audio feedback for impacts
- **Haptic Feedback**: Controller vibration
- **Particle Quality**: Performance vs visual quality trade-off

### Advanced Options

- **Affect Vehicles**: Include/exclude vehicles from simulation
- **Affect Joints**: Include/exclude elevators/doors
- **Protection Mode**: Respect 'leave_me_alone' tags

## API Compatibility

- **Minimum Version**: Teardown 1.4.0
- **Recommended**: Teardown 1.7.0+
- **New Functions Used**:
  - `CreateShape()`, `ClearShape()`, `ResizeShape()`
  - `LoadSound()`, `PlaySound()`
  - `LoadHaptic()`, `PlayHaptic()`
  - Enhanced particle system
  - New UI functions

## Performance Notes

- **Particle Quality**: Lower settings improve performance
- **Protection Mode**: Reduces processing overhead
- **Vehicle Exclusion**: Significantly improves performance in vehicle-heavy maps
- **Real-time Monitoring**: Press F1 during gameplay to see performance stats

## Troubleshooting

### Common Issues

1. **No Sound Effects**: Ensure sound files are in `MOD/sounds/` folder
2. **No Haptic Feedback**: Requires compatible controller with haptic support
3. **Performance Issues**: Reduce particle quality or enable protection mode
4. **Mod Not Loading**: Check Teardown version compatibility

### Debug Information

The mod displays real-time statistics in the top-left corner:

- Bodies processed
- Holes created
- Particles spawned

## Changelog

### v2.0 (Latest)

- Complete rewrite using Teardown 1.4.0+ API
- Material-specific damage system
- Enhanced particle effects
- Sound and haptic feedback
- Modern UI with advanced options
- Performance monitoring
- Creative mode compatibility

### v1.x (Legacy)

- Original momentum-based structural integrity
- Basic particle effects
- Simple configuration options

## Contributing

This mod uses several utility libraries:

- **slimerand.lua**: Fast random number generation
- **slimegcfunc.lua**: Garbage collection utilities

## License

Enhanced by GitHub Copilot based on original work by Litttle_fish.

## Support

For issues or feature requests, please check:

- Teardown modding documentation
- Official Teardown Discord
- Steam Workshop comments
