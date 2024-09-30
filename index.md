---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Overview 
layout: default
order: 1
---

## Knowledge-Informed Machine Learning for Cancer Applications

### Machine Learning for Cancer 

Cancer remains one of the most challenging diseases to treat in the medical field, with its incidence escalating alongside the increasing global life expectancy. Machine learning has enabled in-depth analysis of rich multi-omics profiles and medical imaging for cancer diagnosis and prognosis. Still, cancer applications present several modeling challenges for machine learning models, including the limited labeled sample sizes, the intricate interplay of high-dimensionality data types, the heterogeneity observed among patients and within tumors, and concerns about model interpretability. 

One strategy to tackle these challenges is to integrate biomedical knowledge into machine learning models, referred to as **knowledge informed machine learning (KIML)**. By regularizing the learning process using domain knowledge, the accuracy, robustness, and interpretability of models can be improved. Over the past decase, knowledge-informed machine learning has garnered increasing interest and demonstrated success across scientific, engineering, and health applications, particularly as a solution for settings with limited training data. 

### A Review of KIML for Cancer 

Here, we focus on [knowledge informed machine learning models applied in the cancer domain](https://arxiv.org/abs/2401.06406), where rich biomedical knowledge exists. We reviewed **173** related papers focusing on the past decade, including both machine learning and deep learning studies.


<img src="images/Figure1.png" alt="figure1" width="600" class="center" margin="auto"/>


*Figure 2. Annual trends of knowledge-informed machine learning articles addressing cancer diagnosis and prognosis*


Papers were categorized based on three dimensions:

* *What type of data is used for this application?*
* *In what form is the knowledge represented?*
* *How is the knowledge integrated into the machine learning pipeline?*

An overview of the taxonomy is shown in Figure 2:

<img src="images/Figure2.png" alt="figure2" width="1050" class="center" margin="auto"/>


*Figure 1. Taxonomy of knowledge-informed machine learning in cancer diagnosis and prognosis. Our literature review categorizes existing along three dimensions: type of data, form of knowledge representation, and strategy for knowledge integration. Note that one paper may be included in more than one category. The thickness of the paths indicates the relative frequency of papers in each area (thin: one to four papers; medium: five to nine papers; thick: equal or more than ten papers)*

### Live Summary Table

Below are studies compiled from our [review](https://arxiv.org/abs/2401.06406). This website is meant as a resource for those looking to use knowledge informed machine learning for their application (healthcare or non-health related) but unsure how each component is realized in practice, and an overview of knowledge informed machine learning as an emerging field.

**Use this [link](https://forms.gle/5kpcCzYFpy5vYhGp8) to submit a paper to be added to this table.** 
*Last updated in September, 2024*

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
      		{% if pair[0] == "Paper" %}
      			{% assign beatles = pair[1] | split: "-" %}
      		  <a href = "{{ beatles[1] }}"> {{ beatles[0] }} </a> 
      		{% else %}
      		   {{ pair[1] }}
      		{% endif %}
          {% endtablerow %}
      
    {% endfor %}
</table>

<!-- Include jQuery 
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
-->
<!-- Include DataTables CSS and JS 
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.11.6/css/jquery.dataTables.min.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.11.6/js/jquery.dataTables.min.js"></script>
-->
<!-- Include DataTables Buttons CSS and JS 
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/buttons/2.2.9/css/buttons.dataTables.min.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/buttons/2.2.9/js/dataTables.buttons.min.js"></script>
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/buttons/2.2.9/js/buttons.colVis.min.js"></script>
-->
<link href="https://cdn.datatables.net/1.13.8/css/jquery.dataTables.css" rel="stylesheet">
<link href="https://cdn.datatables.net/buttons/2.4.2/css/buttons.dataTables.css" rel="stylesheet">
<link href="https://cdn.datatables.net/colreorder/1.7.0/css/colReorder.dataTables.css" rel="stylesheet">
<link href="https://cdn.datatables.net/responsive/2.5.0/css/responsive.dataTables.css" rel="stylesheet">
<link href="https://cdn.datatables.net/scroller/2.3.0/css/scroller.dataTables.css" rel="stylesheet">
<link href="https://cdn.datatables.net/select/1.7.0/css/select.dataTables.css" rel="stylesheet">
 
<script src="https://code.jquery.com/jquery-3.7.0.js"></script>
<script src="https://cdn.datatables.net/1.13.8/js/jquery.dataTables.js"></script>
<script src="https://cdn.datatables.net/buttons/2.4.2/js/dataTables.buttons.js"></script>
<script src="https://cdn.datatables.net/colreorder/1.7.0/js/dataTables.colReorder.js"></script>
<script src="https://cdn.datatables.net/responsive/2.5.0/js/dataTables.responsive.js"></script>
<script src="https://cdn.datatables.net/scroller/2.3.0/js/dataTables.scroller.js"></script>
<script src="https://cdn.datatables.net/select/1.7.0/js/dataTables.select.js"></script>

<script type="text/javascript" class="init">
new DataTable('#kiml', {
    paging: true,
    scrollCollapse: false,
    scrollY: '800px',
    scrollX: true,
    //ordering: true,
    buttons: ['copy', 'csv'],
    //autoWidth: true,
    //scroller: {
    //  rowHeight: 20
    //},
    //scroller.rowHeight: 20,
    dom: 'B<"clear">lfrtip',
    columnDefs: [{ "width": "50%", "targets": [3]}]
  });
</script>

  

<br />
<br />




