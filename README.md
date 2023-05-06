Download Link: https://assignmentchef.com/product/solved-ee7207-assignment-2
<br>
<em>Note: You can use MatLab/Simulink or any other software package to perform your simulation.  </em>

<em> </em><strong><u> FUZZY CONTROL. </u></strong>We first consider a truck-parking control problem, as shown in Figure 1.1. The objective is to design a controller, without assuming a mathematical model of the truck, to park the truck anywhere on the <em>x</em>-axis.

Figure 1.1

(a) Suppose that the truck can move forward at a constant speed of <em>v </em>= 0.5 <em>m/s </em>and it is assumed that the truck is  equipped with sensors that can measure location (<em>x,y</em>) and orientation θ (angle) at all times. The fuzzy logic controller is to provide an input, <em>u</em>, to rotate the steering wheels and, consequently, to maneuver the truck from any given initial condition to reach <em>y</em>=θ=0 at the parked position. In the simulation, the input variables are the truck angle and the vertical position coordinate, <em>y</em>, while the output variable is the steering angle (signal), <em>u</em>. The variable ranges are pre-assigned as

–100 ≤ <em>y </em>≤ 100, –180 ≤ θ ≤ 180, –30 ≤ <em>u </em>≤ 30.

Here, clockwise rotations are considered positive in θ, and, therefore, counter-clockwise are negative.

A simplified model to generate the values of (<em>x,y</em>) and orientation θ (angle) can be obtained from the geometry of the truck shown in Figure 1.1 as follows:




(1.1)




where




The linguistic terms used in this design are given as follows:




<h1>                                 <em>y</em>-position                      Angle θ                           Steering angle <em>u</em></h1>




Table 1.1

The associated membership functions for the variables <em>y</em> and θ are shown in Figure 1.2 and 1.3 respectively.

Figure 1.2

θ

Figure 1.3

The rule base used in simulation is summarized in Table 1.2. Each rule has the form IF <em>y </em>is <em>Y </em>AND θ is  THEN <em>u </em>is <em>U</em>, as usual. A glance of these rules reveals the symmetry, an intrinsic property of this controller, which is reasonable for this parking application since the truck can move in any direction.

Table 1.2

The membership function of the control variable <em>u</em> is shown in Figure 1.4.

Figure 1.4

Finally, we need to obtain the output action <em>u</em> under the given input conditions. The following standard Centre of Gravity (COG) defuzzification formula is to be used in the simulation:




<em>u</em><em>i</em> <em>U</em><em>i </em>(<em>u du</em><em>i </em>) <em>i</em>

<em>u</em><em>COG </em>= <em>U                        </em>

<em>U</em><em>i </em>(<em>u du</em><em>i </em>)   <em>i</em>

<em>U</em>




Design a fuzzy logic controller and perform simulations for the following 4 initial conditions and plot out the corresponding<em> u</em>(<em>t</em>), <em>y</em>(<em>t</em>)  and θ(<em>t</em>) to show that <em>y</em> and θ reaches 0 at the end of the parked position.




<table width="501">

 <tbody>

  <tr>

   <td width="73">Case</td>

   <td width="106">1</td>

   <td width="104">2</td>

   <td width="113">3</td>

   <td width="104">4</td>

  </tr>

  <tr>

   <td width="73">θ</td>

   <td width="106">0</td>

   <td width="104">90</td>

   <td width="113">220</td>

   <td width="104">-10</td>

  </tr>

  <tr>

   <td width="73"><em>y</em></td>

   <td width="106">40</td>

   <td width="104">-30</td>

   <td width="113">30</td>

   <td width="104">10</td>

  </tr>

  <tr>

   <td width="73"><em>x </em></td>

   <td width="106">20</td>

   <td width="104">10</td>

   <td width="113">40</td>

   <td width="104">50</td>

  </tr>

 </tbody>

</table>




Table 1.3







(b) For the given model in Equation (1.1), design a classical non-fuzzy logic controller to reach <em>y</em>=θ=0 given the same 4 initial conditions listed in Table 1.3 and plot out the results.

<ol start="2">

 <li><u></u><u> <strong>CLUSTERING.</strong></u> Clustering is one of the most fundamental issues in pattern recognition. It plays a key role in searching for structures in data. Given a finite set of data, <strong>X</strong>, the problem of clustering in <strong>X</strong> is to find several cluster centres that can properly characterize relevant classes of <strong>X</strong>. In classical cluster analysis, these classes are required to form a partition of <strong>X</strong> such that the degree of association is strong for data within blocks of the partition and weak for data in different blocks. However, this requirement is too strong in many practical applications, and it is thus desirable to replace it with a weaker requirement. When the requirement of a crisp partition of <strong>X</strong> is replaced with a weaker requirement of a fuzzy partition or a fuzzy pseudopartition on <strong>X</strong>, we refer to the emerging problem area as fuzzy clustering. Fuzzy pseudopartitions are often called fuzzy c partitions, where c designates the number of fuzzy classes in the partition. There are two basic methods of fuzzy clustering. One of them, which is based on fuzzy c-partitions, is called a fuzzy c-means (FCM) clustering method. However, the fuzzy c-means method requires that the desired number of clusters be specified. This is a disadvantage whenever the clustering problem does not specify any desired number of clusters. In such problems, the number of clusters should reflect, in a natural way, the structure of given data. The other method, based on fuzzy equivalence relations, is called a fuzzy equivalence relation-based hierarchical clustering method, works in this way.</li>

</ol>




<h1>2.1 Cosine Amplitude</h1>




Given a set of data array <strong>X</strong>,




<strong>X</strong> = {<em>x</em><sub>1</sub>, <em>x</em><sub>2</sub>, …, <em>x</em><sub>n</sub>}




where each of the elements <em>x<sub>i</sub></em> in the data array <strong>X</strong> is a vector of length <em>m</em>, that is,




<em>x<sub>i </sub></em>=<sub></sub><em>x<sub>i</sub></em>1 <em>x<sub>i</sub></em>2







Fuzzy relations map elements from Cartesian product of 2 universes to [0,1] where the strength of the relation is expressed by the membership function of the relation. Let <strong>R</strong> defined on <em>X</em> <em>X</em> be a binary fuzzy relation from single universe <em>X</em> to the same universe <em>X</em>. Each element of a relation <strong><em>R</em></strong>, <em>r<sub>ij</sub></em>, results from a pairwise comparison of 2 data samples, say <em>x<sub>i</sub></em> and <em>x<sub>j</sub></em>, where the strength of the relationship between data samples <em>x<sub>i</sub></em> and <em>x<sub>j</sub></em> is given by the membership value expressing that strength, that is <em>r<sub>ij</sub></em> = μ<strong><em><sub>R</sub></em></strong>(<em>x<sub>i</sub></em>, <em>x<sub>j</sub></em>). This relation matrix <strong><em>R</em></strong> will be of size <em>n</em> x <em>n </em>and relates the similarity of the data samples.




The cosine amplitude method is a useful similarity method to calculate and ensures that the resultant relation <strong><em>R</em></strong> will be symmetric and reflexive and is in fact a tolerance relation (see Section 2.2). It calculates <em>r<sub>ij</sub></em> in the following manner:




<em>m</em>

<em>x x</em><em>ik  jk</em>

<em>r</em><em><sub>ij </sub></em>=          <em><sup>k</sup></em><sup>=</sup><sup>1                                      </sup>   ,       where ,<em>i j </em>=1, 2,       , <em>n</em>                                             (2.1)

 <em>m </em><em>x</em>2  <em>m </em><em>x</em>2<em>jk </em>

      <em>ik </em>

 <em>k</em>=1         <em>k</em>=1         




Close inspection of Equation (2.1) reveals that this method is related to the dot product for the cosine function. When 2 vectors are collinear (most similar), their dot product is unity; when the 2 vectors are at right angles to one another (most dissimilar), their dot product is zero.







<h1>2.2 Fuzzy Equivalence Relation</h1>




<em>R</em> is a <strong>fuzzy equivalence relation</strong> (also known as similarity relation) if <strong><u>all</u></strong> of the following 3 properties are satisfied:




<ul>

 <li>Reflexive : <em><sub>R </sub></em>(<em>x x</em><em><sub>i</sub></em>, <em><sub>i </sub></em>)=1 for all <em>x X</em><em><sub>i </sub></em> .</li>

 <li>Symmetric : <em><sub>R </sub></em>(<em>x x</em><em><sub>i</sub></em>, <em><sub>j </sub></em>)=<em><sub>R </sub></em>(<em>x x</em><em><sub>j </sub></em>, <em><sub>i </sub></em>) for all ,<em>x x</em><em><sub>i              j </sub></em><em>X</em>.</li>

 <li>Transitive : <em><sub>R </sub></em>(<em>x x</em><em><sub>i </sub></em>, <em><sub>j </sub></em>)= <sub>1</sub> and <em><sub>R </sub></em>(<em>x x</em><em><sub>i </sub></em>, <em><sub>j </sub></em>)= <sub>2 </sub>→ <em><sub>R </sub></em>(<em>x x</em><em><sub>i </sub></em>, <em><sub>k </sub></em>) min(<sub>1</sub>, <sub>2</sub>) for all ,<em>x x x</em><em><sub>i   j </sub></em>, <em><sub>k </sub></em><em>X</em>.</li>

</ul>




A <strong>fuzzy tolerance relation</strong>, <em>R</em><sub>1</sub> defined on <em>X</em>  <em>X</em>, has properties of reflexivity and symmetry.  <em>R</em><sub>1 </sub>can be transformed into a fuzzy equivalence relation <em>R</em> by <strong><em><u>at most</u></em></strong> (<em>n</em>-1) compositions where <em>n</em> is the cardinality of <em>X</em>. That is




<em>m</em>−2

<em>R</em><sub>1</sub><em><sup>m </sup></em>=<em>R</em><sub>1</sub>             <em>R R</em><sub>1 </sub>=  where <em>m n</em> −1




Example 2.1: The following fuzzy tolerance relation <em>R</em><sub>1</sub>

<table width="171">

 <tbody>

  <tr>

   <td width="60">  </td>

   <td width="28"> </td>

   <td width="28"> </td>

   <td width="28"> </td>

   <td width="27"> </td>

  </tr>

  <tr>

   <td width="60"> 1<sup></sup>0.8 <em>R</em><sub>1 </sub>=0.40.5 <sub></sub>0.2</td>

   <td width="28">0.8 10.40.50.9</td>

   <td width="28">0.40.4 10.40.4</td>

   <td width="28">0.50.50.4 10.5</td>

   <td width="27">0.20.9<sup></sup>0.40.51 <sub></sub></td>

  </tr>

 </tbody>

</table>




is easily seen to be both reflexive and symmetric. However, it is not transitive, for example,




<em><sub>R</sub></em>(<em>x x</em><sub>1 2</sub>,  )= 0.8, <em><sub>R</sub></em>(<em>x x</em><sub>2</sub>, <sub>5</sub>)= 0.9 but <em><sub>R</sub></em>(<em>x x</em><sub>1 5</sub>, )= 0.2  min 0.8,0.9( ) .




A single composition operation results in







<table width="270">

 <tbody>

  <tr>

   <td width="114"> 1<sup></sup>0.8 <em>R R R</em><sub>1</sub><sup>2 </sup>= <sub>1 1 </sub>=0.40.5<sub></sub>0.8 </td>

   <td width="30">0.8 10.40.50.9</td>

   <td width="30">0.40.4 10.40.4</td>

   <td width="30">0.50.50.4 10.5</td>

   <td width="66">0.80.9<sup></sup>0.4=<em>R</em>   ,0.51 <sub></sub></td>

  </tr>

 </tbody>

</table>

is transitive since <em><sub>R </sub></em>(<em>x x</em><em><sub>i </sub></em>, <em><sub>j </sub></em>)= <sub>1</sub> and <em><sub>R </sub></em>(<em>x x</em><em><sub>i </sub></em>, <em><sub>j </sub></em>)= <sub>2 </sub>→ <em><sub>R </sub></em>(<em>x x</em><em><sub>i </sub></em>, <em><sub>k </sub></em>) min(<sub>1</sub>, <sub>2</sub>)  for all ,<em>x x x</em><em><sub>i j </sub></em>, <em><sub>k </sub></em><em>X</em>.

<table width="295">

 <tbody>

  <tr>

   <td width="114">Furthermore, </td>

   <td width="29"> </td>

   <td width="29"> </td>

   <td width="34"> </td>

   <td width="89"> </td>

  </tr>

  <tr>

   <td width="114"> 1<sup></sup>0.8 <em>R R R</em>13 = 1    12 =0.40.5<sub></sub>0.8</td>

   <td width="29">0.8 10.40.50.9</td>

   <td width="29">0.40.4 10.40.4</td>

   <td width="34">0.50.50.4 10.5</td>

   <td width="89">0.80.9<sup></sup>0.4= <em>R R</em><sub>1</sub><sup>2 </sup>=  .0.51 <sub></sub></td>

  </tr>

 </tbody>

</table>







Hence, a simple algorithm to transform a fuzzy tolerance relation <em>R</em><sub>1 </sub>into a fuzzy equivalence relation <em>R</em> is as follows:




<strong>Algorithm 2.1 </strong>




<ol>

 <li><em>R R R</em><sup>‘ </sup>= <sub>1</sub></li>

 <li>If <em>R R</em><sup>‘ </sup> <sub>1</sub>, assign <em>R R</em><sub>1 </sub>= <sup>‘</sup> and goto Step 1.</li>

 <li>Else Stop: <em>R R</em>= <sup>‘</sup></li>

</ol>




<h1>2.3 <em>α</em>-Compatibility Class</h1>




It can be shown that if <em>R</em> is a fuzzy equivalence relation (also known as similarity relation) then each <em>α</em>-cut <em>R<sub>α</sub></em> is a crisp equivalence relation. Effectively, then, we may use any fuzzy equivalence relation <em>R</em> and by taking any <em>α</em>cut <em>R<sub>α</sub></em> for any value (0,1 , create a crisp equivalence relation that represents the presence of similarity between the elements to the degree <em>α</em>. Each of these equivalence relations forms a partition of <em>X</em>.




Example 2.2: Let us illustrate this clustering approach with <em>X</em> = {<em>x</em><sub>1</sub>, <em>x</em><sub>2</sub>, <em>x</em><sub>3</sub>, <em>x</em><sub>4</sub>, <em>x</em><sub>5</sub>} and using <em>α</em>-cut <em>R<sub>α</sub></em> on the fuzzy equivalence relation <em>R</em> in Example 2.1.




<table width="158">

 <tbody>

  <tr>

   <td width="52"> 1<sup></sup>0.8 <em>R</em>=0.40.5<sub></sub>0.8</td>

   <td width="27">0.8 10.40.50.9</td>

   <td width="27">0.40.4 10.40.4</td>

   <td width="27">0.50.50.4 10.5</td>

   <td width="26">0.8 0.90.40.51 <sub></sub></td>

  </tr>

 </tbody>

</table>




By taking <em>α</em>-cut <em>R<sub>α</sub></em> of fuzzy equivalence relation <em>R</em> at values of <em>α</em> = 1, 09, 0.8, 0.5 and 0.4, we get the following:




1 0 0 0 0                  1 0 0 0 0              1   1    0    0    1

<sup></sup>0 1 0 0 0<sup></sup>,                 <sup></sup>0 1 0 0 1<sup> </sup>,            1  1    0    0  1 ,

<em>R</em><sub>1 </sub>=0 0 1 0 0 <em>R</em><sub>0.9 </sub>=0 0 1 0 0 <em>R</em><sub>0.8 </sub>=0                               0    1    0    0

<sub></sub>0 0 0 1 0              0 0 0 1 0           0  0    0    1  0

<sub></sub>0 0 0 0 1<sub>              </sub><sub></sub>0 1 0 0 1<sub>           </sub><sub></sub>1  1    0    0  1<sub></sub>







1 1 0 1 1                 1 1 1 1 1

1 1 0 1 1             1 1 1 1 1

,

<em>R</em><sub>0.5 </sub>=0 0 1 0 0 <em>R</em><sub>0.4 </sub>=1 1 1 1 1

                                               

1 1 0 1 1                 1 1 1 1 1

<sub></sub>1 1 0 1 1<sub>             </sub><sub></sub>1 1 1 1 1<sub></sub>




We can see that the clustering of the five data points according to the <em>α</em> level is as shown in Table 2.1







<table width="416">

 <tbody>

  <tr>

   <td width="142"><em>α</em>-cut level</td>

   <td width="274">Classification Results</td>

  </tr>

  <tr>

   <td width="142">1.0</td>

   <td width="274">{<em>x</em><sub>1</sub>},{<em>x</em><sub>2</sub>},{<em>x</em><sub>3</sub>},{<em>x</em><sub>4</sub>},{<em>x</em><sub>5</sub>}</td>

  </tr>

  <tr>

   <td width="142">0.9</td>

   <td width="274">{<em>x</em><sub>1</sub>},{<em>x</em><sub>2</sub>, <em>x</em><sub>5</sub>},{<em>x</em><sub>3</sub>},{<em>x</em><sub>4</sub>}</td>

  </tr>

  <tr>

   <td width="142">0.8</td>

   <td width="274">{<em>x</em><sub>1</sub>, <em>x</em><sub>2</sub>, <em>x</em><sub>5</sub>},{<em>x</em><sub>3</sub>},{<em>x</em><sub>4</sub>}</td>

  </tr>

  <tr>

   <td width="142">0.5</td>

   <td width="274">{<em>x</em><sub>1</sub>, <em>x</em><sub>2</sub>, <em>x</em><sub>4</sub>, <em>x</em><sub>5</sub>},{<em>x</em><sub>3</sub>}</td>

  </tr>

  <tr>

   <td width="142">0.4</td>

   <td width="274">{<em>x</em><sub>1</sub>, <em>x</em><sub>2</sub>, <em>x</em><sub>3</sub>, <em>x</em><sub>4</sub>, <em>x</em><sub>5</sub>}</td>

  </tr>

 </tbody>

</table>




Table 2.1 Classification of 5 data points according to <em>α</em>-cut level




We can also express the classification results described in Table 2.1 with a tree classification diagram as shown in Figure 2.1. In the figure, it can be observed that the higher the value of <em>α</em>, the finer is the classification. As <em>α</em> gets larger, the results of fuzzy classification approach the trivial case when each data point is assigned to its own class.










Figure 2.1 Classification Tree







<u>2.4 Problem.</u> 16 districts in a country have suffered flooding from a recent thunderstorm. The flooding in each district are characterized according to three flooding levels : mild (&lt;0.1 m),  moderate (0.1 to 0.2 m), severe (0.2 to 0.3 m), catastrophic (&gt; 0.3 m). The percentage of areas within a given district with each of the flooding levels is given in Table 2.2.













Table 2.2 Flooding Levels in 16 Districts







<ul>

 <li>Use the cosine method in Equation (2.1) of Section 2.1 to generate the fuzzy tolerance relation <em>R</em><sub>1</sub>.</li>

 <li>Use Algorithm 2.1 in Section 2.2 to transform <em>R</em><sub>1</sub> into a fuzzy equivalence relation <em>R</em>.</li>

 <li>Generate the <em>α</em>-cut <em>R<sub>α</sub></em> in Section 2.3 to provide classification classes for <em>α</em>-cut level = 0.4 and <em>α</em>-cut level =</li>

</ul>

0.8?

<ul>

 <li>If we want to classify the flooding for the whole county into 3 classes – <strong>Red, </strong><strong>Yellow and </strong><strong>Green</strong>. What should be the appropriate the <em>α</em>-cut value?</li>

</ul>