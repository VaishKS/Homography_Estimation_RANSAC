# RANSAC Homography Estimation

## Input

<div align="center">
<p>
<img src="images/keble_a.jpg" width="200"/><img src="images/keble_b.jpg" width="200"/><img src="images/keble_c.jpg" width="200"/>
</p>
<br>
</div>

## Steps

Merge the above images into a Mosaic as follows:

<ul>
  <li>Choose one image as the reference image frame.</li>
  <li>Estimate a homography between each of the remaining images and the reference one. Each homography estimation is done by:
    <ul>
      <li>Detecting local features in each image</li>
      <li>Matching feature descriptors between two images</li>
      <li>Estimating the homography between two images with RANSAC for robustness to wrong keypoint correspondences</li>
    </ul>
  </li>
  <li>Warping each image into the reference frame using the estimated homography and composite the warped images into a single mosaic</li>
</ul>

## Merged Image using SIFT Descriptors

<div align="center">
<p>
<img src="results/sift-stitched.jpg" width="400"/>
</p>
<br>
</div>

## Merged Image using FAST Descriptors

<div align="center">
<p>
<img src="results/fast-stitched.jpg" width="400"/>
</p>
<br>
</div>
