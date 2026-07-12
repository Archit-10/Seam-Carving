# Seam-Carving

## Introduction

Seam carving is a smart image resizing technique that changes the size of an image without simply stretching or cropping it. Instead, it removes the least important pixels while keeping important objects and edges intact.

<h2><strong>Features</strong></h2>

- Energy Calculation: Computes the energy of each pixel in the image, enabling effective seam identification.
- Seam Identification: Identifies the seam (path of pixels) with the lowest energy to minimize distortion.
- Seam Removal: Removes the identified seam from the image to achieve the desired dimensions.
- Resizing: Continuously removes seams until the image reaches the specified size.
- User Input: Allows users to specify the desired width or height for resizing.
- Multiple Energy Functions: Supports different methods for calculating energy, such as gradient magnitude and color histograms.

<h2><strong>Demonstration</strong></h2>
<p>Before and after images showcasing the seam carving effect.</p>

<p>The input image is on the left and the result is on the right.</p>

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/a5fd7851-9a96-49bb-a0a9-60b8972aff66" width="500"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c4277ee1-de84-40f8-8e04-36216566b1d8" width="200"/>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/1420848c-34c3-48de-a5de-2cad5600bb8d" width="500"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/becca250-4f0c-4b67-be7d-e3f1f1896741" width="200"/>
    </td>
  </tr>
</table>

## Build Instructions

### Requirements
- C++17 or higher
- OpenCV
- CMake

### Build Steps

```bash
git clone https://github.com/Archit-10/content-aware-image-resizing.git
cd content-aware-image-resizing

mkdir build
cd build

cmake ..
make
```

## Run the Program

Run the executable:

```bash
./seam_carver
```

When prompted, enter the target image dimensions in the following format:

```text
width height
```

**Example:**

```text
400 300
```

The resized image will be saved to:

```text
assets/output/resized.png
```

<h2><strong>Performance Metrics</strong></h2>

- Time Complexity: O(NM) for finding the optimal seam, where N is the height and M is the width of the image.
- Memory Usage: Memory usage is proportional to the size of the image, as additional space is required for energy and cost matrices.

## Challenges & Solutions

- **Challenge:** Preserving important edges and objects during seam removal in complex images.
- **Solution:** Used a gradient-based energy function to prioritize significant visual regions and minimize distortion.

## QA 

- Verified energy computation on sample images
- Tested seam removal across multiple resizing iterations
- Visually inspected output quality after resizing

## Tech Stack

- Programming Language: C++
- Libraries: OpenCV

<h2><strong>Contributions</strong></h2>

Contributions are welcome! If you would like to contribute to this project, please follow these guidelines:

- Fork the repository.

- Create a new branch for your feature or bug fix.

- Submit a PR detailing your changes.    



