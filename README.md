The slides of presentation: *CS530_FinalProject_Presentation_slides.pdf*

The implementation of project: folder *code* and folder *ParaView*

Dataset: 

ftp_path: ftp://hpc-ftp.lanl.gov/data/visualization/

Other path: https://oceans11.lanl.gov/firetec/

How to run state file from *ParaView*: 

Open ParaView, On the top left corner, click *file*, then cilck *Load_State...*, and then choose *ParaView*. Upon opening, ParaView would require then path to the wildfire folder. Make sure the files are preprocessed by *preprocess.py*, and ParaView would be able to handle time series information automatically. 

In folder *ParaView*:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*para_state.pvsm*

In folder *code*:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*main.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to explore the dataset's information. Everything we got is in the comments on the very top of this Python file.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python main.py

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*preprocessing.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to convert .vts files to .vti files. The file path defined in the code.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python preprocessing.py

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*iso_theta.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to visualize the scalar field *theta* with isosurfacing.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python iso_theta.py [-i|--input] \<vti_file\>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*volume_render_theta.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to visualize the scalar field *theta* with volume rendering.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python volume_render_theta.py [-i|--input] \<vti_file\>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Combined_with_slider.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to visualize the scalar fields *rohf_1* and *theta* at the same time. A slider is used to control *rohf_1* value to find the best visualization for grass.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: python Combined_with_slider.py [-i|--input] \<vti_file\>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Combined.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Same as *Combined_with_slider.py* but without a slider. A fixed *rohf_1* value is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python Combined.py [-i|--input] \<vti_file\>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*file_browser_backcurve.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Same as *Combined.py*, plus a slider to control which file is used. Specifically used to backing fire.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python file_browser_backcurve.py

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*file_browser_headcurve.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Same as *file_browser_headcurve.py*. Specifically used to head fire.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python file_browser_backcurve.py

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*script_back.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to generate same visualziation (*Comnbined.py*) for all the backing fire .vti files. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python script_back.py

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*script_head.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to generate same visualziation (*Comnbined.py*) for all the head fire .vti files. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python script_head.py

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*wind.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Used to discover how to extract the scalar fields for the wind and convert them to a vector field.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python wind.py [-i|--input] \<vti_file\>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Combined_with_wind.py*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Same as *Combine.py*, plus the converted wind field, which is visualized with Glyph.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run: > python Combined_with_wind.py [-i|--input] \<vti_file\>
