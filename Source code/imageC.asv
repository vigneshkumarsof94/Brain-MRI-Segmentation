function x = imageC(image1,image2,image3,image4,image5,image6)
figure(1)
imshow(image1)
figure(2)
imshow(image2)
figure(13)
imshow(image3)
figure(4)
imshow(image4)
figure(5)
imshow(image5)
figure(6)
imshow(image6)

distance=zeros(256,256);


for i=1:256
    for j=1:255
        distance(i,j) = abs(image3(i,j) - image3(i,j+1));
    end
end
redMatrix = zeros(256,256);
blueMatrix = zeros(256,256);
greenMatrix = zeros(256,256);
for i=1:256
    for j=1:255
        if((distance(i,j)>=0)&&(distance(i,j)<85))
            redMatrix(i,j)=43;
        elseif((distance(i,j)>=85)&&(distance(i,j)<170))
            blueMatrix(i,j)=128;
        elseif((distance(i,j)>=170)&&(distance(i,j)<256))
            greenMatrix(i,j)=213;
        end
    end
end
redImage = cast(cat(3, redMatrix, zeros(size(redMatrix)), zeros(size(redMatrix))), class(redMatrix));
greenImage = cast(cat(3, zeros(size(greenMatrix)), image3, zeros(size(greenMatrix))), class(greenMatrix));
blueImage = cast(cat(3, zeros(size(blueMatrix)), zeros(size(blueMatrix)), image3), class(blueMatrix));
figure(2)
RGB_IM = cat(3, redImage(:,:,1), greenImage(:,:,2), blueImage(:,:,3));

figure(7)
imshow(RGB_IM)

end