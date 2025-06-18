# Dot-Pixelate a Profile Photo

Use the Jupyter notebook to turn a blank background photo of a subject (e.g., a png photo) into:
- A dot pixel photo of the subject, and
- A dots and sticks background photo with the original subject.


## To Create a Hover-and-Reveal Effect
You can use the two output photos to achieve a hover-and-reveal effect to display a photo of you in your personal website. To achieve that, refer to the following codes:
```
<div className="cover-photo-container">
  <Image src={DotPortrait1} alt="Dot Pixel Photo" className="cover-photo" />
  <Image src={DotPortrait2} alt="Revealed Photo" className="cover-photo" />
</div>
```
and accompanying css styling:
```
.cover-photo-container .cover-photo:last-child {
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
}

.cover-photo-container:hover .cover-photo:first-child {
  opacity: 0;
}

.cover-photo-container:hover .cover-photo:last-child {
  opacity: 1;
}
```
