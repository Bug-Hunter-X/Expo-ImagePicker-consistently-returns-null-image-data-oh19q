# Expo ImagePicker Null Result Bug

This repository demonstrates a bug encountered when using the Expo ImagePicker library.  The picker functions correctly, allowing users to select images, but the returned image data is consistently null.  This issue occurs despite having the necessary permissions and selecting valid images.

## Reproducing the Bug

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on a real device or emulator.
4. Select an image using the image picker.
5. Observe that the resulting image data is null.

## Potential Solutions

The solution involves using the `uri` property directly obtained from the picker's response object instead of attempting to get the image data. The `uri` property offers a direct path to access the selected image.

## Note

This bug is likely caused by some unforeseen interaction between Expo ImagePicker and the underlying image handling mechanisms.  This solution offers a workaround; a more definitive fix would require investigation into Expo's image picker implementation.