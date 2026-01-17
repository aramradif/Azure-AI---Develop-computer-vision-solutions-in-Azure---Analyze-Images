# Azure-AI---Develop-computer-vision-solutions-in-Azure---Analyze-Images
Provision an Azure Vision resource and use it from a client application to analyze images

Use Azure Vision's image analysis capabilities in scenarios that require information extraction or inference from images. 

A common use case is digital asset management (DAM), in which you need to tag, catalog, and index image-based data.

Python development language

from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.ai.vision.imageanalysis.models import VisualFeatures
from azure.core.credentials import AzureKeyCredential

client = ImageAnalysisClient(
    endpoint="<YOUR_RESOURCE_ENDPOINT>",
    credential=AzureKeyCredential("<YOUR_AUTHORIZATION_KEY>")
)

result = client.analyze(
    image_data=<IMAGE_DATA_BYTES>, # Binary data from your image file
    visual_features=[VisualFeatures.CAPTION, VisualFeatures.TAGS],
    gender_neutral_caption=True,
)


