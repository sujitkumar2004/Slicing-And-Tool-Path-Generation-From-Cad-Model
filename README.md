# 🛠️ Slicing and Tool Path Generation for Layered Manufacturing

This project demonstrates the generation of CNC-compatible tool paths from 3D CAD models using MATLAB. It simulates a layered manufacturing workflow — starting from STL conversion to contour slicing, spiral path planning, and G-code generation. The final tool paths are validated on CNC machines for manufacturability and accuracy.

---

## 📌 Objective

To build a computational pipeline that:
- Converts CAD models to STL mesh
- Extracts planar slice contours
- Generates optimized spiral tool paths
- Detects bottom/contact points for precise cutting
- Exports G-code for CNC machines

---

## 🧰 Technologies Used

- **MATLAB** – algorithm development & toolpath logic
- **CAD/STL** – model input format
- **G-code** – machine-readable instructions
- **CNC Machine** – toolpath validation platform

---

## 📁 Folder Structure

.
├── src/
│ ├── stl_parser.m # Extracts 3D mesh from STL
│ ├── slicer.m # Slices model at given height
│ ├── contour_extraction.m # Extracts and organizes 2D cross-sections
│ ├── toolpath_generator.m # Generates spiral paths
│ ├── gcode_writer.m # Exports G-code
│ └── utils.m # Common helper functions
├── sample_models/
│ └── demo_part.stl
├── output/
│ └── demo_part.gcode
├── cnc_demo/
│ └── validation_video.mp4
├── report.pdf
└── README.md


---

## 🧪 Methodology

1. **STL Conversion**  
   - CAD models exported in STL format using standard CAD software.

2. **Slicing**  
   - Performed planar slicing to extract contours at each Z-layer.

3. **Bottom/Contact Point Detection**  
   - Located critical surfaces where material removal begins.

4. **Toolpath Generation**  
   - Implemented spiral trajectory logic to ensure minimal tool wear.

5. **G-code Output**  
   - Wrote layer-wise instructions compatible with CNC execution.

6. **Validation**  
   - Executed toolpaths on CNC and verified dimensional accuracy.

---

## 🎥 Demo

▶️ [Click here to watch CNC execution demo](https://drive.google.com/file/d/1dsl-TIqtJVyNKrJ3ihg5uD7RlYB-9d6f/view?usp=drivesdk)

---

## 🚀 How to Run

### Requirements:
- MATLAB (R2021a or later recommended)

### Steps:
```matlab
% Load STL and slice
slicer('sample_models/demo_part.stl', 0.5); 

% Generate toolpath
toolpath_generator('output/sliced_data.mat');

% Export G-code
gcode_writer('output/toolpath.mat');


📈 Key Features
🔄 CAD to STL compatibility

✂️ Precise cross-sectional slicing

🔁 Spiral tool path optimization

⚙️ G-code generation for CNC

✅ Physical validation on CNC hardware

🧠 Bottom/contact-aware deformation logic

🎓 Academic Context
This project was conducted under the supervision of Prof. Anirban Bhattacharya as part of a mechanical engineering practicum at IIT Patna.
