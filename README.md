This is an example of using MediaPipe AAR in Android Studio with Gradle.

The steps to build and use MediaPipe AAR is documented in MediaPipe's [android_archive_library.md](https://github.com/google/mediapipe/blob/master/docs/getting_started/android_archive_library.md). 

To build aar file.
bazel build -c opt --strip=ALWAYS     --host_crosstool_top=@bazel_tools//tools/cpp:toolchain     --fat_apk_cpu=arm64-v8a,armeabi-v7a mediapipe/examples/android/src/java/com/google/mediapipe/apps/aar_example:mediapipe_pose_tracking --verbose_failures

To build binarypb:
bazel build -c opt --strip=ALWAYS --host_crosstool_top=@bazel_tools//tools/cpp:toolchain     --fat_apk_cpu=arm64-v8a,armeabi-v7a mediapipe/graphs/pose_tracking:pose_tracking_gpu_binary_graph

The binarypb is in the folder
/bazel-bin/mediapipe/graphs/pose_tracking



1. To control the output stream, you can modify https://github.com/google/mediapipe/blob/master/mediapipe/graphs/pose_tracking/pose_tracking_gpu.pbtxt to generate your own pose_tracking_gpu.binarypb, then overwrite it in the folder app/src/main/assets/

2. Google ML Kit Pose detection.
   > https://developers.google.com/ml-kit/vision/pose-detection

3. After my testing, the current Mediapipe pose detection model is more accurate than ML Kit even if Google said ML Kit also uses BlazePose.
