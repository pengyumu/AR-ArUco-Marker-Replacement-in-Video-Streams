# AR-ArUco-Marker-Replacement-in-Video-Streams


The goal is to replace ArUco markers detected in a video with predefined images or patches. Please see below for the steps that were taken during the implementation.

•	Importing Libraries: OpenCV, NumPy, and Matplotlib are imported for handling video pro-cessing and visualization tasks.
•	Reading Video and Initializing Parameters: The cv2.VideoCapture function is used to read the input video file (aruco.mp4). Video properties like frame rate (fps), width, and height are obtained using cap.get.VideoWriter object is initialized to write the processed frames into an output video file (outputvideo.mp4) using the MP4V codec.
•	Loading ArUco Marker Dictionary and Image Patches: cv2.aruco.getPredefinedDictionary is used to load the predefined dictionary for ArUco markers.Image patches for each ArUco marker ID are loaded into a dictionary.
•	Marker Detection and Replacement: Inside a loop, each frame of the input video is read and processed.The frame is converted to grayscale for marker detection.ArUco markers are de-tected using cv2.aruco.detectMarkers.If markers are detected, replacement images are resized and warped onto the marker positions using homography.The replacement frame is then written into the output video using out.write.
•	Visualization and Display: After processing each frame, it is displayed using Matplotlib’s imshow function to visualize the replaced markers.A short pause (cv2.waitKey) is added to dis-play the frames correctly within the notebook.
•	Release Resources: After processing all frames, resources like VideoCapture and VideoWriter objects are released using cap.release() and out.release().
