This is an example of using MediaPipe AAR in Android Studio with Gradle.

The steps to build and use MediaPipe AAR is documented in MediaPipe's [android_archive_library.md](https://github.com/google/mediapipe/blob/master/docs/getting_started/android_archive_library.md). 

1. To control the output stream, you can modify https://github.com/google/mediapipe/blob/master/mediapipe/graphs/pose_tracking/pose_tracking_gpu.pbtxt to generate your own pose_tracking_gpu.binarypb, then overwrite it in the folder app/src/main/assets/
