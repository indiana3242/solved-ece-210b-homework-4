Download Link: https://assignmentchef.com/product/solved-ece-210b-homework-4
<br>



<ol>

 <li>Professor Mintchev has just assigned you 20 tedious Gram Schmidt Orthonormalization problems! Luckily, you are a master of MATLAB so you decide to build a function which can handle them all for you in short time. <strong>Note: </strong>This homework has been assigned in all three ECE-210 sections.</li>

</ol>

<ul>

 <li>Create a function called <em>gramSchmidt</em>. The input to the function should be a 2-D array, each column of which is a vector in the original linearly independent set of vectors. Implement GS to create an orthonormal set of vectors from these. Store them as columns in an output matrix, similar to the input format. Feel free to use the <em>norm </em>function if needed.</li>

 <li>After you’ve created this function, you’d like a way to test if it works. Create another function called <em>isOrthonormal </em>which has a single 2-D array as the input. The function should return 1 if all columns are orthonormal and 0 otherwise. Be careful with this – direct floating point equality comparison is a bad idea. Instead apply a threshold to the difference of the two numbers like so: ifthen … The <em>eps </em>function might be useful here. You can add a nice big fudge factor to make the tolerance big enough that it works, just don’t make it huge. (Note that there is also the matter of spanning the same space as the original matrix, don’t worry about this condition)</li>

 <li>Finally, we would like to estimate another vector as a linear combination of these orthonormal vectors. (Project the vector onto the space of the orthonormal vectors.) Implement a function called <em>orthoProj </em>which takes a vector to be estimated and and array of orthonormal columns as arguments and outputs the estimated vector.</li>

 <li>Test all of the above functions on some random complex vectors. (use <em>rand </em>to make a random vector) First test the case where there are more elements in each vector than the number of vectors. Then test the case where the number of vectors is equal to the number of elements in a vector. Compare the errors.</li>

 <li>Uniformly sample <em>sin(x) </em>on [0<em>,</em>2<em>π</em>]. Generate 5 Gaussians with the equation</li>

</ul>

Give each Gaussian standard deviation 1 (<em>σ </em>= 1) and pick the mean from a linearly spaced vector ranging from 0 to 2<em>π</em>. (<em>µ </em>∈ {0<em>,π/</em>2<em>,π,</em>3<em>π/</em>2<em>,</em>2<em>π</em>}) Consider using <em>ndgrid </em>for compact code. Plot the Sinusoid and Gaussians on the same plot. Give axis labels and a title. Use <em>gramSchmidt </em>to create an orthonormal set of vectors from the Gaussians. Use orthoProj to estimate the sinusoid from that set of vectors. Create a 2×1 subplot. Plot the sinusoid and the estimated sinusoid together on the upper plot. Plot the orthonormal basis functions on the lower plot. Give all plots proper labels and titles.

1