# art_inpainting
art_inpainting aim to help art research or fans to repair the damaged art painting such as damaged Dunhuang-murals.

# how to
to repair or inpaint the damaged area of painting could be classify to two main categories:
1. small damage (such as small holes, crease etc), which means people can use features or information of just that paint to repair the small damage
2. big damage (such as big hole etc), which means people hardly can only use features or information of the damaged paint to repair the paint, people have to reference by know-how, knowledge and creative to do the work

so, I want to make an AI inpainting tool which have such powers:  
**have enough art feature knowledge-base, such as art style, art pattern etc. and AI can reference that knowlege-base to do the repair or inpainting**

# high level design
1. art semantic search on art components database:  
people can talk to AI to get the proper art components from database.that's a vector database, every components are embedded to vector and stored in order to be searched
1. inpaint workbench:  
people can use this workbench to do art inpainting or repair
1. mint NFT:  
people can mint their valuble work (such as component or repaired art etc) to NFT
# detailed design
## Art Semantic Search
1. use SAM to segment the art paint to get components
1. annotate the component, such as: detailed description of components
## inpaint workbench
use Gradio as framework to build the app  
### main steps
1. annotate the area needed to do repairing or inpainting
2. choose the inpainting AI model and decide the param of model 
3. choose the referrence knowledge from database
4. run inpainting or repairing