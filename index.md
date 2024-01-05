---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
order: 1
---
# Knowledge-Informed Machine Learning for Cancer Applications

Cancer remains one of the most challenging diseases to treat in the medical field, with its incidence escalating alongside the increasing global life expectancy. Machine learning has enabled in-depth analysis of rich multi-omics profiles and medical imaging for cancer diagnosis and prognosis. Despite these advancements, machine learning models face challenges stemming from limited labeled sample sizes, the intricate interplay of high-dimensionality data types, the inherent heterogeneity observed among patients and within tumors, and concerns about interpretability and consistency with existing biomedical knowledge. 

To address these challenges, a viable strategy involves the integration of biomedical knowledge into machine learning models, referred to as **knowledge-informed machine learning**. By regularizing the model’s learning process using domain knowledge (or models of that knowledge), the accuracy, robustness, and interpretability of models can be improved. Over the past decase, knowledge-informed machine learning has garnered increasing interest and demonstrated success across scientific, engineering, and health applications, particularly as a solution for settings with limited training data. In the realm of cancer biology and oncology research, there is a growing demand for the integration of mechanistic models, a form of biomedical knowledge, and machine learning.

This review focuses on the application of knowledge-informed machine learning in the cancer domain, where rich biomedical knowledge exists to navigate the aforementioned modeling challenges. The scope encompasses both traditional machine learning and deep learning models utilized for cancer diagnosis and prognosis, employing input data (X) such as gene expression profiles or medical images to predict clinical outcomes (y), such as cancer phenotype or patient risk score. An extensive search was conducted on PubMed in April 2023, focusing on original research articles published from 2012 onward (within the last 10 years). 

[Here, we survey 127 studies]in knowledge-informed machine learning in the cancer domain, focusing on original research articles published from 2012 onward (within the last 10 years). We provide an overview of diverse forms of knowledge representation and current strategies of knowledge integration into machine learning pipelines with concrete examples. 

![align="center"](images/Figure2.png)
*Taxonomy of knowledge-informed machine learning in cancer diagnosis and prognosis. Our literature review categorizes existing along three dimensions: type of data, form of knowledge representation, and strategy for knowledge integration. Note that one paper may be included in more than one category. The thickness of the paths indicates the relative frequency of papers in each area (thin: one to four papers; medium: five to nine papers; thick: equal or more than ten papers*

Below are studies from our [review paper]. This website is meant as (1) a resource to those looking to use knowledge-informed machine learning for their application but unsure how each component is realized in practice, and (2) a map of knowledge-informed machine learning as an emerging field.

**This table is live meaning anyone can submit a study to be considered for this table** and we will update the table **every week**. Entries are grouped by application area. 

## Use this [link](https://forms.gle/ACBwCCfH6UzTeaBZ8) to submit a study to be added to this table.

<br />

<table id = "kiml" class="display">
  {% for row in site.data.mgl %}
      {% if forloop.first %}
        <thead>
        <tr>
          {% for pair in row %}
            <th>{{ pair[0] }}</th>
          {% endfor %}
        </tr>
        </thead>
      {% endif %}
    
        {% tablerow pair in row %}
      		{% if pair[0] == "Method" %}
      			{% assign beatles = pair[1] | split: "-" %}
      		  <a href = "{{ beatles[1] }}"> {{ beatles[0] }} </a> 
      		{% else %}
      		   {{ pair[1] }}
      		{% endif %}
          {% endtablerow %}
      
    {% endfor %}
</table>


<script type="text/javascript" class="init">
$(document).ready(function() {
  // Create a new DataTable object
  table = $('#kiml').DataTable();
});
</script>

  

<br />
<br />




