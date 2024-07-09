# Shader-Graphs-Part-3

## Workflow and Process for the Unlit Shader and Lit Shader

### Unlit Shader Screenshot

![HK_UnlitShaderGraph](https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/28e7d164-0266-49f6-b21c-fc109cc45502)

### Graph View
https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/761f0983-d706-484b-a9e8-6157337abe97

### Game View
https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/71f7ff46-8fef-42c3-88b1-bfe7886c4cc3

### VR View
https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/77eecdcd-1e33-47f1-8e27-2ba6e9744139

The Unlit Shader Graph is a simplified shader designed for objects that do not require lighting calculations. Here is a detailed workflow that I used in creating the Unlit Shader:

- **Time Node**: This node provides time-based animation. It generates a time-based sine wave, creating oscillating values.
- **Sine Wave Calculation**: The sine wave values are multiplied to adjust their amplitude and combined with a vector to control the UV offset.
- **Polar Coordinates**: Converts the UV space to polar coordinates, enabling a circular texture manipulation effect.
- **Timing and Offset**: The calculated values from the time node and sine wave are used to offset the UV coordinates dynamically, creating an animated texture effect.
- **Texture Sampling**: A texture is sampled and mapped using the modified UV coordinates, resulting in a swirling animation effect.
- **Final Output**: The texture is directly passed to the Unlit Master node, which outputs the final unlit shader without any lighting calculations.

### Lit Shader Screenshot

![HK_LitShaderGraph](https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/a3f0af1f-dd08-4b67-b880-31a0c371cd12)

### Graph View
https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/6d409cbb-a926-40f7-93ae-e94df62b59c3

### Game View
https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/c84c244c-e162-4319-b2c4-6abf00cff078

### VR View
https://github.com/hamidakhatri/Shader-Graphs-Part-3/assets/43552885/8123c615-986e-4aae-8259-1c56f708e186

The Lit Shader Graph is more complex, involving lighting calculations for realistic shading. The workflow that I used includes:

- **Time Node**: Similar to the Unlit Shader, a time node generates a sine wave for animated effects.
- **Texture Sampling**: Two textures are sampled, one for the base color and another for additional effects like normal mapping.
- **Polar Coordinates**: Converts UV space to polar coordinates for a circular manipulation effect.
- **Timing and Offset**: Uses sine wave calculations to dynamically offset UV coordinates, creating an animated texture.
- **Normal Mapping**: A normal map texture is sampled and combined with vertex normals to affect the lighting calculations.
- **PBR Master Node**: Inputs like base color, normal, metallic, smoothness, and occlusion are connected to the PBR Master node, which performs physically-based rendering calculations for realistic lighting and shading effects.
 
These shader graphs effectively demonstrate the creation of both basic unlit shaders and more complex lit shaders with animated effects and realistic lighting that I really enjoyed developing.
