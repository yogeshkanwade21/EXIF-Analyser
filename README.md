# EXIF-Analyser
A Python script to extract and analyse EXIF data.

## Table of Contents

1. [Introduction](#introduction)
2. [How to Use](#how-to-use)
3. [Sample Images](#sample-images)
4. [ExifTool](#exiftool)
5. [Questions](#questions)
6. [Contributors](#contributors)

## Introduction
* This project is a part of SPPU final year Cyber Security and Digital Forensics course.
* The main aim behind this project is to dive into the world of digital forensics.

## How to Use
If you want to try using this project, here is a step-by-step guide. 

<details>
<summary>
Step 1: Clone It
</summary>

- **Using Git** 

Open your terminal and run the following command:

```bash
git clone https://github.com/yogeshkanwade21/EXIF-Analyser.git
```

- **Using Download ZIP**

1. Go to the GitHub page of the repository.
2. Click on the green **Code** button.
3. In the dropdown menu, select **Download ZIP**.

</details>

---
<details>
<summary>
Step 2: Install Dependencies
</summary>

Before you begin playing with the source code, you might need to install dependencies just as shown below;

```bash
pip install -r requirements.txt
```
**Note**
* You might want to consider creating a virtual environment.
* If you are wondering how to go about generating requirements.txt for your projects, <a href="https://github.com/bndr/pipreqs" target="_blank">try checking this out.</a>

</details>

---
<details>

<summary>
Step 3: Run
</summary>

Navigate to the directory and run the streamlit app.

```bash
streamlit run script.py
```

</details>

## Sample Images

* Sample images for testing Exif metadata retrieval can be found <a href="https://github.com/ianare/exif-samples" target="_blank">here.</a>

## ExifTool
* ExifTool is a free and open-source software program for reading, writing, and manipulating meta information. <a href="https://exiftool.org/" target="_blank">Check it out here.</a>

## Questions

<details>
  <summary>
    What is digital forensics?
  </summary>
  Digital forensics is the process of collecting, analyzing, and preserving electronic evidence to investigate and prevent cybercrime or other digital incidents. It involves examining digital devices, such as computers, smartphones, or servers, to uncover and interpret data that can be used in legal proceedings. Digital forensics experts use specialized tools and techniques to recover, analyze, and document digital evidence, helping to understand the timeline and details of digital activities related to a case.
</details>

---

<details>
  <summary>
    What is EXIF?
  </summary>
  EXIF stands for Exchangeable Image File Format. It is a standard that specifies the formats for images, sound, and ancillary tags used by digital cameras (including smartphones), scanners, and other systems handling image and sound files recorded by digital cameras. EXIF data typically includes information such as the date and time the photo was taken, camera settings (such as shutter speed and aperture), GPS location data (if available), and other details about the camera and its settings. This metadata can be useful for organizing and understanding the context of digital images.
  EXIF data is structured within the metadata of digital image files, and it follows a specific format based on the TIFF (Tagged Image File Format) structure. The metadata is organized in a series of tags, each with a unique identifier (tag number) and a corresponding value. These tags contain information about various aspects of the image, such as camera settings, timestamps, GPS coordinates, and more.
</details>

---

<details>
  <summary>
    What is the role of EXIF data in image forensics?
  </summary>
  EXIF data plays a crucial role in image forensics, aiding investigators and analysts in understanding the context and authenticity of digital images. Here are some ways in which EXIF data is utilized in image forensics:

1. **Authentication and Integrity Verification:**
   - **Timestamps:** EXIF data includes timestamps indicating when the photo was taken. This information can help verify the timeline of events and establish the authenticity of images in investigations.
   - **Digital Signatures:** Some camera models embed digital signatures or unique identifiers in the EXIF data, providing a means to verify the source and integrity of the image.

2. **Camera and Device Attribution:**
   - **Make and Model Information:** EXIF data often contains details about the make and model of the camera or device used to capture the image. This can assist in attributing images to specific devices.
   - **Serial Numbers:** Some cameras embed serial numbers in the EXIF data, offering additional information for tracking and identification.

3. **Location Analysis:**
   - **GPS Coordinates:** If available, GPS information in EXIF data provides the geographic location where the photo was taken. This can be crucial in investigations involving physical locations or establishing an individual's presence at a specific place.

4. **Event Reconstruction:**
   - **Exposure Settings:** Details like exposure time, aperture, and ISO settings in the EXIF data can provide insights into the conditions under which the image was captured. This information is valuable for reconstructing events and understanding the circumstances of the photo.

5. **Tampering Detection:**
   - **Edit History:** Some image editing software updates the EXIF data when modifications are made. Analyzing the EXIF metadata can reveal if and how an image has been altered.
   - **Thumbnail Discrepancies:** Comparing the thumbnail image in the EXIF data with the actual image can help detect discrepancies that may indicate tampering.

6. **Consistency Checks:**
   - **Inconsistencies in Metadata:** Analyzing the EXIF data for inconsistencies, such as conflicting timestamps or illogical camera settings, can raise flags and prompt further investigation.

</details>


---

<details>
  <summary>
    Is EXIF same as metadata?
  </summary>
  Yes, EXIF (Exchangeable Image File Format) is a specific type of metadata. Metadata, in a broad sense, refers to data that provides information about other data. In the context of digital media, including images, videos, and documents, metadata contains details about the file itself or the content it represents.
  EXIF metadata, specifically, is the type of metadata associated with digital images. It includes information such as the date and time the photo was taken, camera settings, GPS coordinates (if available), and other details related to the creation of the image. While EXIF is specific to images, metadata can refer to a broader range of information associated with different types of files.
</details>

---

<details>
  <summary>
    Is EXIF a file format or extension?
  </summary>
  EXIF (Exchangeable Image File Format) is not a file format or extension on its own. Instead, it is a standard that specifies the formats for images and the associated metadata tags used by digital cameras, scanners, and other systems handling image files.
  Typically, EXIF data is embedded within the file of a supported image format, such as JPEG or TIFF. So, when you have an image file (e.g., a .jpg file), the EXIF information is contained within that file as metadata, providing details about the image and how it was captured. It's essentially an additional layer of information within the existing image file format rather than a separate file format or extension.
</details>

---

<details>
  <summary>
    Does every image have EXIF data?
  </summary>
No, not every image has EXIF data. The presence of EXIF data depends on the settings of the device used to capture the image and the file format of the image itself. Most digital cameras, including smartphones, embed EXIF data by default when capturing photos. However, if someone intentionally removes or modifies the metadata, or if the image is edited and saved in a way that discards the original metadata, the EXIF information may be missing.  
Images from certain sources or edited images may lack EXIF data, and some image-sharing platforms may strip or modify this information for privacy or security reasons. Therefore, while it's common in images captured by digital cameras, it's not universal across all images.
</details>

---

<details>
  <summary>
    What are other formats of metadata in images apart from EXIF?
  </summary>
  Apart from EXIF, there are other formats of metadata associated with images. Two notable ones are:

1. **IPTC (International Press Telecommunications Council):** IPTC metadata is commonly used in the photography and news industry. It includes information such as captions, keywords, and copyright details. While EXIF focuses on technical details related to the image capture, IPTC metadata is more geared towards descriptive and administrative information.

2. **XMP (Extensible Metadata Platform):** XMP is a standard created by Adobe Systems. It allows for the embedding of metadata in various file formats, including images. XMP is extensible and can accommodate a wide range of information, from basic details like copyright and authorship to more complex data like image processing history. XMP is often found in conjunction with other metadata formats, including EXIF.

These metadata formats may coexist within an image file, providing a comprehensive set of information about the content, its creation, and usage. Each format serves specific purposes, contributing different types of data to enhance the understanding and management of digital assets.
  </details>
  
---

<details>
  <summary>
    Is EXIF data human readable?
  </summary>
EXIF data is not typically designed to be human-readable in its raw form. It consists of numerical tags and values encoded in a binary format within the image file. While these numerical codes are meaningful to software and applications that interpret them, they may not be easily understandable for the average person. However, many photo viewing and editing software tools provide a user-friendly representation of EXIF data. They present the information in a more readable format, often alongside the image. This allows users to view details such as the date and time the photo was taken, camera settings, and, if available, geolocation information in a human-friendly manner.
</details>

---

<details>
  <summary>
    What is geolocation tag in EXIF?
  </summary>
  The geolocation information in EXIF is typically represented by a group of tags related to GPS data. Here are the key numeric EXIF tags associated with geolocation:

1. **GPS Latitude (GPSLatitude):** `2`
2. **GPS Longitude (GPSLongitude):** `4`
3. **GPS Altitude (GPSAltitude):** `6`
4. **GPS Time (GPSTimeStamp):** `29`
5. **GPS Date (GPSDateStamp):** `29`

These tags collectively provide details about the geographic coordinates (latitude, longitude), altitude, and timestamp of when the GPS data was recorded. Keep in mind that not all images may have GPS information, as it depends on whether the camera or device used for capturing the image has GPS capabilities and if the user has enabled location services.
</details>

---

<details>
  <summary>
    What are some examples of EXIF tags?
  </summary>
  
1. **Exif Version (ExifVersion):** `36864`

2. **Date and Time (DateTimeOriginal, DateTimeDigitized):** `36867`, `36868`

3. **Camera Make (Make):** `271`

4. **Camera Model (Model):** `272`

5. **Exposure Time (ExposureTime):** `33434`

6. **Aperture (FNumber):** `33437`

7. **ISO Speed (ISOSpeedRatings):** `34855`

8. **Focal Length (FocalLength):** `37386`

9. **GPS Information (GPSLatitude, GPSLongitude):** `2`, `4`

10. **Orientation (Orientation):** `274`

11. **Flash Information (Flash):** `37385`

These numeric tags are used in the EXIF data structure to represent specific metadata elements within an image file.
</details>

---

<details>
  <summary>
    Can EXIF data be manipulated?
  </summary>
  Yes, EXIF data can be altered. It is not inherently secure or tamper-proof, and various methods and tools exist that allow users to modify or delete EXIF information from digital image files. This ability to alter EXIF data raises considerations for its reliability, especially in situations where the authenticity of the data is crucial.
</details>

---

<details>
  <summary>
    How can EXIF data be manipulated?
  </summary>

Common methods for altering EXIF data include:

1. **Image Editing Software:**
   - Many image editing applications provide functionality to view and modify EXIF data. Users can edit timestamps, camera settings, and other metadata directly within these programs.

2. **Online Tools:**
   - There are online tools and websites that offer EXIF editing services. Users can upload an image and modify its metadata using a web-based interface.

3. **Command-Line Tools:**
   - Command-line tools and scripts exist that allow users to manipulate EXIF data. These tools are often used by individuals with a technical background who want to automate the process of altering metadata.

4. **Metadata Stripping:**
   - Some social media platforms and image-sharing websites automatically strip or modify EXIF data from uploaded images for privacy and security reasons. This process may inadvertently alter or remove information.

</details>

---

<details>
  <summary>
    How reliable is EXIF data?
  </summary>
    If the image is sourced directly from a camera or a trusted device, and the EXIF data has not been tampered with, it is generally considered reliable. However, if the image has been shared, edited, or passed through various platforms, there's a risk that the EXIF data may have been altered or stripped.
    While the ability to alter EXIF data is a known limitation, forensic experts and investigators are aware of this issue. In legal and forensic contexts, additional steps are taken to verify the authenticity of digital evidence. This may involve cross-referencing information from multiple sources, conducting forensic analysis, and using other metadata or contextual clues to establish the credibility of the data.
  While EXIF data can be a valuable source of information, especially for understanding the context and details of an image, it should be used with caution, and its reliability should be assessed in the context of the specific use case. For critical applications, additional verification methods and a comprehensive analysis of the entire digital asset may be necessary.
</details>
  
## Contributors
* <a href="https://github.com/yogeshkanwade21">Yogesh Kanwade</a>
* <a href="https://github.com/kshitijkasabekar">Kshitij Kasabekar</a>
