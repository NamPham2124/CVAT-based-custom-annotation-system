\# CVAT-based Custom Annotation System 



Dự án là tuỳ chỉnh lại hệ thống CVAT



\## Features

* Công cụ chú thích được lược giản hoá dễ sử dụng 



\## Quick start 🚀



\### Step 1 : Hiểu cấu trúc cvat-ui



\*\*Note\*\* : All UI features được thực hiện ở 'cvat-ui/src/components/annotation-page/'



\*\*Structure\*\* :

```

annotation-page/

├── annotation-page.tsx              # Main annotation page router

├── top-bar/                         # Top navigation bar

│   ├── top-bar.tsx                  # Main top bar component

│   ├── left-group.tsx               # Left buttons (Undo/Redo/Save/Done)

│   ├── right-group.tsx              # Right buttons (Fullscreen/Guide/Info/Filters/Workspace)

│   ├── annotation-menu.tsx          # Main menu dropdown

│   ├── player-buttons.tsx           # Play/Pause/Navigation buttons

│   ├── player-navigation.tsx        # Frame slider/input

│   └── save-annotations-button.tsx  # Save button component

│

├── standard-workspace/              # Main annotation workspace (2D)

│   ├── standard-workspace.tsx       # Main workspace container

│   ├── controls-side-bar/           # Left sidebar with drawing tools

│   │   ├── controls-side-bar.tsx    # Main controls container

│   │   ├── tools-control.tsx        # AI/ML tools button

│   │   ├── opencv-control.tsx       # OpenCV tools button

│   │   ├── draw-rectangle-control.tsx

│   │   ├── draw-polygon-control.tsx

│   │   ├── draw-polyline-control.tsx

│   │   ├── draw-points-control.tsx

│   │   ├── draw-ellipse-control.tsx

│   │   ├── draw-cuboid-control.tsx

│   │   ├── draw-mask-control.tsx

│   │   ├── draw-skeleton-control.tsx

│   │   ├── merge-control.tsx        # Merge shapes tool

│   │   ├── group-control.tsx        # Group shapes tool

│   │   ├── split-control.tsx        # Split track tool

│   │   ├── join-control.tsx         # Join shapes tool

│   │   ├── slice-control.tsx        # Slice track tool

│   │   └── cursor-control.tsx       # Cursor/select tool

│   │

│   └── objects-side-bar/            # Right sidebar

│       ├── objects-side-bar.tsx     # Main sidebar container

│       ├── objects-list.tsx         # List of annotated objects

│       └── labels-list.tsx          # List of labels

│

├── standard3D-workspace/            # 3D annotation workspace

├── single-shape-workspace/          # Single shape annotation mode

├── tag-annotation-workspace/        # Tag-only annotation mode

├── attribute-annotation-workspace/  # Attribute editing mode

├── review-workspace/                # Review/QC workspace

│

├── canvas/                          # Canvas rendering components

│   ├── grid-layout/                 # Canvas layout configuration

│   └── views/

│       ├── canvas2d/                # 2D canvas components

│       └── canvas3d/                # 3D canvas components

│

└── review/                          # Review/QC components

&nbsp;   ├── issues-aggregator.tsx        # Issues display component

&nbsp;   └── create-issue-dialog.tsx      # Issue creation dialog

```

\### STEP2 : Xác định các tính năng cần xoá 

* \*\*DrawRectangleControl\*\*
* \*\*DrawPolygonControl\*\*
* \*\*DrawPolylineControl\*\*
* \*\*DrawPointsControl\*\*
* \*\*DrawEllipseControl\*\*
* \*\*DrawCuboidControl\*\*
* \*\*DrawMaskControl\*\*
* \*\*DrawSkeletonControl\*\*
* \*\*SetupTagControl\*\*
* \*\*JoinControl\*\*
* \*\*SplitControl\*\*
* \*\*SliceControl\*\*
* \*\*Filter\*\*

\### STEP3 : Thực hiện 

Đối chiếu các tính năng muốn xoá hoặc không cần thiết ở STEP2 với cấu trúc ở STEP1 để tìm file xoá các tính năng không cần thiết

example : remove Filter --> tìm feature Filter trong structure --> sửa code ở top-bar/right-group.tsx



&nbsp;

