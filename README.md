Smoke Detection Prototype — Retinex + YOLOv9 + ByteTrack + Smoke Validation
Garay & Rañola

Upload a video, pick a model, and the prototype runs the full Config 3 pipeline on it: Retinex enhancement → YOLOv9 detection → ByteTrack → Section 3.4 smoke validation. It returns an annotated video, a verdict, and a timeline of detections.

The Retinex functions, tracker, and validation checks are copied from the thesis notebook, so the prototype behaves the same way as the evaluated pipeline.

How to use

Runtime → Change runtime type → GPU.
Run all cells top to bottom (Runtime → Run all).
Open the public Gradio link printed by the last UI cell (or use the inline app).
Upload a video, choose a model, click Run detection.
Box colors in the output video

Yellow (thin): raw YOLOv9 detection, with confidence
Blue: tracked region (ByteTrack ID and persistence score P)
Red (thick): confirmed smoke — passed persistence + all Section 3.4 checks
