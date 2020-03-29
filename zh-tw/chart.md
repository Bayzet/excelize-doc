# �D��

## ��ӈD�� {#AddChart}

```go
func (f *File) AddChart(sheet, cell, format string, combo ...string) error
```

�����o���Ĺ��������Q����������˺͈D���ʽ���Բ���D��

������ Excelize ֧�ք����ĈD��e `type`��

���Q|�D��e
---|---
area                        | ���S�^��D
areaStacked                 | ���S�ѯB�^��D
areaPercentStacked          | ���S�ٷֱȶѯB�^��D
area3D                      | ���w�^��D
area3DStacked               | ���w�ѯB�^��D
area3DPercentStacked        | ���w�ٷֱȶѯB�^��D
bar                         | ���SȺ�M�l�ΈD
barStacked                  | ���S�ѯB�l�ΈD
barPercentStacked           | ���S�ٷֱȶѯB�l�ΈD
bar3DClustered              | ���wȺ�M�l�ΈD
bar3DStacked                | ���w�ѯB�l�ΈD
bar3DPercentStacked         | ���w�ٷֱȶѯB�l�ΈD
bar3DConeClustered          | ���wȺ�Mˮƽ�A�F�D
bar3DConeStacked            | ���w�ѯBˮƽ�A�F�D
bar3DConePercentStacked     | ���w�ѯB�ٷֱ�ˮƽ�A�F�D
bar3DPyramidClustered       | ���wȺ�Mˮƽ���F�D
bar3DPyramidStacked         | ���w�ѯBˮƽ���F�D
bar3DPyramidPercentStacked  | ���w�ѯB�ٷֱ�ˮƽ���F�D
bar3DCylinderClustered      | ���wȺ�Mˮƽ�A���D
bar3DCylinderStacked        | ���w�ѯBˮƽ�A���D
bar3DCylinderPercentStacked | ���w�ѯB�ٷֱ�ˮƽ�A���D
col                         | ���SȺ�M���ΈD
colStacked                  | ���S�ѯB���ΈD
colPercentStacked           | ���S�ٷֱȶѯB���ΈD
col3D                       | ���w���ΈD
col3DClustered              | ���wȺ�M���ΈD
col3DStacked                | ���w�ѯB���ΈD
col3DPercentStacked         | ���w�ٷֱȶѯB���ΈD
col3DCone                   | ���w�A�F�D
col3DConeClustered          | ���wȺ�M�A�F�D
col3DConeStacked            | ���w�ѯB�A�F�D
col3DConePercentStacked     | ���w�ٷֱȶѯB�A�F�D
col3DPyramid                | ���w���F�D
col3DPyramidClustered       | ���wȺ�M���F�D
col3DPyramidStacked         | ���w�ѯB���F�D
col3DPyramidPercentStacked  | ���w�ٷֱȶѯB���F�D
col3DCylinder               | ���w�A���D
col3DCylinderClustered      | ���wȺ�M�A���D
col3DCylinderStacked        | ���w�ѯB�A���D
col3DCylinderPercentStacked | ���w�ٷֱȶѯB�A���D
doughnut                    | �hȦ�D
line                        | �۾��D
pie                         | �A�ΈD
pie3D                       | ���w�A�ΈD
radar                       | ���_�D
scatter                     | ɢ�шD
surface3D                   | ���w����D
wireframeSurface3D          | ���w����D��ֻ�@ʾ���l��
contour                     | ����D
wireframeContour            | ����D����ҕ��ֻ�@ʾ���l��
bubble                      | ���݈D
bubble3D                    | ���w���݈D

�� Office Excel �ЈD���Y�υ^�� `series` ָ�����L����Щ�Y�ϵ���Ϣ���ϡ��D��헣�ϵ�У���ˮƽ������S�˻`��

������ Excelize �� `series` �Ŀ��x������

����|���x
---|---
name|�D��헣�ϵ�У����ڈD��D���͹�ʽ�����@ʾ��`name` �����ǿ��x�ģ������ָ��ԓֵĬ�J����ʹ�� `Series 1 .. n` ��ʾ��`name` ֧��ʹ�ù�ʽ��ʾ�����磺`Sheet1!$A$1`��
categories|ˮƽ������S�˻`���ڴ�����D��e�У�`categories` �����ǿ��x�ģ�Ĭ�J������ `1..n` ���B�m���С�
values|�D���Y�υ^���� `series` ������Ҫ�ą�����Ҳ�Ǆ����D��rΨһ�ı��x������ԓ�x헌��D���c���@ʾ�Ĺ������Y��朽�����
line |�O���۾��D���۾���ʽ��`line` �����ǿ��x�ģ����δָ��ԓ���ԣ��t��Ĭ�J��ʽ�������O�����x��� `width`�����ȹ����� 0.25pt �� 999pt����� `width` ��ֵ�����������t����Ĭ�J���Ȟ� 2pt��

���� `legend` �ṩ���D��헵Č����O�������������� Excelize �� `legend` �Ŀ��x������

����|e|���x
---|---|---
position|string|�D��λ��
show_legend_key|bool|�@ʾ�D���������c�D���دB

���Ѕ��� `position` Ĭ�Jֵ�� `right`�������ǿ��xֵ��

���xֵ|���x
---|---
top|����
bottom|����
left|����
right|����
top_right|����

���Ѕ��� `show_legend_key` Ĭ�Jֵ�� `false`��

ͨ�^���x `title` ����� `name` �����O���D����}�����}�����ڈD���Ϸ��@ʾ������ `name` ֧��ʹ�ù�ʽ��ʾ������ `Sheet1!$A$1`���D����}��Ĭ�Jֵ��ա�

���� `show_blanks_as` �ṩ���[�غ���Ճ�����O����Ĭ�Jֵ�飺`gap` �����Ճ�����@ʾ�项�����վࡹ��������ԓ�����Ŀ��xֵ��

ֵ|���x
---|---
gap|�վ�
span|��ֱ���B���Y���c
zero|��ֵ

���� `format` �ṩ���D��ƫ�ơ��s�š��ߌ����O���ʹ�ӡ���Եȅ������O�����䅢���c�� [`AddPicture()`](image.md#AddPicture) ��������ʹ�õ���ͬ��

ͨ�^���x `plotarea` �����O���Y�Ϙ˻`��ʽ�����x�������£�

����|e|Ĭ�Jֵ|���x
---|---|---|---
show_bubble_size|bool|`false`|���ݴ�С
show_cat_name|bool|`true`|e���Q
show_leader_lines|bool|`false`|�@ʾ������
show_percent|bool|`false`|�ٷֱ�
show_series_name|bool|`false`|ϵ�����Q
show_val|bool|`false`|ֵ

ͨ�^���� `x_axis` �� `y_axis` �����O�������S�x헡�

������ `x_axis` �����Ŀ��xֵ��

����|e|Ĭ�Jֵ|���x
---|---|---|---
major_grid_lines|bool|`false`|��Ҫ�W��
minor_grid_lines|bool|`false`|��Ҫ�W��
tick_label_skip|int|`1`|ָ���˻`�g���λ
reverse_order|bool|`false`|����̶�ֵ
maximum|int|`0`|���ֵ��`0` �����Ԅ�
minimum|int|`0`|��Сֵ��`0` �����Ԅ�

������ `y_axis` �����Ŀ��xֵ��

����|e|Ĭ�Jֵ|���x
---|---|---|---
major_grid_lines|bool|`false`|��Ҫ�W��
minor_grid_lines|bool|`false`|��Ҫ�W��
major_unit|float64|`0`|�����S��Ҫ�̶Ȇ�λ
reverse_order|bool|`false`|����̶�ֵ
maximum|int|`0`|���ֵ��`0` �����Ԅ�
minimum|int|`0`|��Сֵ��`0` �����Ԅ�

ͨ�^���x `dimension` �����O���D��Ĵ�С�����x�������£�

����|e|Ĭ�Jֵ|���x
---|---|---|---
height|int|290|�߶�
width|int|480|����

���� `combo` �Á�ָ�������M�ψD��ԓ�D�팢�ɂ�������D��e�M����һ���D���С����磬�� `Sheet1!$E$1:$L$15` �^�򄓽�һ�� Ⱥ�M���ΈD - �۾��D��

```go
package main

import "github.com/360EntSecGroup-Skylar/excelize"

func main() {
    categories := map[string]string{"A2": "Small", "A3": "Normal", "A4": "Large", "B1": "Apple", "C1": "Orange", "D1": "Pear"}
    values := map[string]int{"B2": 2, "C2": 3, "D2": 3, "B3": 5, "C3": 2, "D3": 4, "B4": 6, "C4": 7, "D4": 8}
    f := excelize.NewFile()
    for k, v := range categories {
        f.SetCellValue("Sheet1", k, v)
    }
    for k, v := range values {
        f.SetCellValue("Sheet1", k, v)
    }
    if err := f.AddChart("Sheet1", "E1", `{"type":"col","series":[{"name":"Sheet1!$A$2","categories":"","values":"Sheet1!$B$2:$D$2"},{"name":"Sheet1!$A$3","categories":"Sheet1!$B$1:$D$1","values":"Sheet1!$B$3:$D$3"}],"format":{"x_scale":1.0,"y_scale":1.0,"x_offset":15,"y_offset":10,"print_obj":true,"lock_aspect_ratio":false,"locked":false},"legend":{"position":"left","show_legend_key":false},"title":{"name":"Ⱥ�M���ΈD - �۾��D"},"plotarea":{"show_bubble_size":true,"show_cat_name":false,"show_leader_lines":false,"show_percent":true,"show_series_name":true,"show_val":true}}`, `{"type":"line","series":[{"name":"Sheet1!$A$4","categories":"Sheet1!$B$1:$D$1","values":"Sheet1!$B$4:$D$4"}],"format":{"x_scale":1.0,"y_scale":1.0,"x_offset":15,"y_offset":10,"print_obj":true,"lock_aspect_ratio":false,"locked":false},"legend":{"position":"left","show_legend_key":false},"plotarea":{"show_bubble_size":true,"show_cat_name":false,"show_leader_lines":false,"show_percent":true,"show_series_name":true,"show_val":true}}`); err != nil {
        println(err.Error())
        return
    }
    // �����퓲�
    if err := f.SaveAs("Book1.xlsx"); err != nil {
        println(err.Error())
    }
}
```

## �����D������ {#AddChartSheet}

```go
func (f *File) AddChartSheet(sheet, format string, combo ...string) error
```

�����o���Ĺ��������Q�͈D���ʽ���Ԅ����D�������D���ʽ���ԵĶ��x�c [AddChart](chart.md#AddChart) ������ͬ��Excel �еĈD�������ǃH�����D��Ĺ�����

## �h���D�� {#DeleteChart}

```go
func (f *File) DeleteChart(sheet, cell string) (err error)
```

�����o���Ĺ��������Q�̓�������˄h���D��
