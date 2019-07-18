---

copyright:
  years: 2014, 2019
lastupdated: "2019-07-09"

keywords:

subcollection: image-templates

---


{:new_window: target="_blank"}
{:tip: .tip}
{:faq: data-hd-content-type='faq'}

# FAQs: Image templates
{: #faq-image-templates}

## What is a Standard Image template?
{: faq}

A Standard Image template is the {{site.data.keyword.virtualmachineslong}} imaging option for {{site.data.keyword.BluSoftlayer_notm}}.
Standard image templates allow users to capture an image of an existing virtual server regardless of its operating system and create a new
virtual server based on the image.

## What is an ISO Template?
{: faq}

The ISO Template is a type of template that is specifically reserved for ISOs that can be used to boot a VSI. ISO templates are available in two versions: public and private. Public ISO Templates are preconfigured templates that are provided by {{site.data.keyword.BluSoftlayer_notm}} and can be used by any customer. Private ISO Templates are created by importing an image of an ISO stored on an {{site.data.keyword.objectstorageshort}} Account. In order for an ISO to be imported to the Image Templates screen, the ISO must be bootable.

Only {{site.data.keyword.BluSoftlayer_notm}} Supported Operating Systems can be used to load an ISO template onto a VSI. For more information, see [Supported Operating Systems ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/server-software).
{:tip}

## What is the difference between a Public Image and a Private Image?
{: faq}

A Public Image is an image that can be viewed and applied to a new virtual server by any {{site.data.keyword.BluSoftlayer_notm}} user. {{site.data.keyword.BluSoftlayer_notm}}
currently creates public images as a solution for configuration options on different devices. Customers can also make images public and available to any user. A Private Image is an image that can be
viewed only by authorized users. Authorized users default to any user on your account; however, images also can be shared between multiple
accounts by updating the sharing options in the {{site.data.keyword.cloud_notm}} console.

## Can I capture and deploy virtual servers with my self-managed hypervisor?
{: faq}

Only servers that are provisioned by {{site.data.keyword.BluSoftlayer_notm}} can be captured and deployed. Individual virtual servers that you manually created on personal devices cannot be captured, provisioned, or deployed.

## Can I share my private ISO Template with other customers?
{: faq}

The only ISO Templates that are made public to all customers are templates that are generated by {{site.data.keyword.BluSoftlayer_notm}}. Private ISO Templates are account-specific and cannot be shared between customers through the {{site.data.keyword.cloud_notm}} console.

## Does my ISO template need to be in the same data center as my virtual server to complete a boot from image?
{: faq}

Yes, ISO templates must be in the same data center as a virtual server to boot from the image. If it is not in the same data center,
the ISO template must be copied to the appropriate data center to complete the action. If this situation occurs, a warning
appears regarding the transaction. When an ISO template is copied to a different data center, a small fee is charged to the account in the
same manner that fees are applied for copying other types of image templates.

## What is the difference between physical data and volume size?
{: faq}

Volume is the disk space that is available for storing files, while physical data consists of the actual files that are stored on the disk.

## What is the image import/export feature?
{: faq}

The image import/export feature that is located on the Image Templates page in the {{site.data.keyword.cloud_notm}} console allows for the conversion of VHDs and ISOs stored on an {{site.data.keyword.objectstorageshort}} account to be converted into image templates, and vice versa. When you import an image, a specific file (either VHD or ISO) is sourced from a specified [{{site.data.keyword.objectstorageshort}}] Account's Container and is converted into an image template. The image template can then be used to boot or load a device. When you export an image, the image template is converted into a file (or several files if the template has multiple disks) that is stored in a specified location on an {{site.data.keyword.objectstorageshort}} Account's Container.

## How do I create an image template for my entire server and not just my primary drive?
{: faq}

To create an image template for your entire server, see the instructions in [Creating an image template](/docs/infrastructure/image-templates?topic=image-templates-creating-an-image-template#creating-an-image-template).

If you choose to export an image template to IBM Cloud Object Storage, each block device (or disk) has its own associated file. For example, if your image file is named image.vhd, the first block device is exported as image-0.vhd. The second block device is exported as image-1.vhd, and so on.
{: tip}