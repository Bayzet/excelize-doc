# Variables

```go
var (
    // ErrStreamSetColWidth definió el mensaje de error en el ancho de columna
    // establecido en el modo de escritura de flujo.
    ErrStreamSetColWidth = errors.New("must call the SetColWidth function before the SetRow function")
    // ErrColumnNumber definió el mensaje de error al recibir un número de
    // columna no válido.
    ErrColumnNumber = fmt.Errorf(`the column number must be greater than or equal to %d and less than or equal to %d`, MinColumns, MaxColumns)
    // ErrColumnWidth definió el mensaje de error al recibir un ancho de
    // columna no válido.
    ErrColumnWidth = fmt.Errorf("the width of the column must be less than or equal to %d characters", MaxColumnWidth)
    // ErrOutlineLevel definió el mensaje de error al recibir un número de
    // nivel de esquema no válido.
    ErrOutlineLevel = errors.New("invalid outline level")
    // ErrCoordinates definió el mensaje de error en la longitud de las tuplas
    // de coordenadas no válidas.
    ErrCoordinates = errors.New("coordinates length must be 4")
    // ErrExistsWorksheet definió el mensaje de error en una hoja de trabajo
    // determinada que ya existe.
    ErrExistsWorksheet = errors.New("the same name worksheet already exists")
    // ErrTotalSheetHyperlinks definió el mensaje de error sobre el
    // desbordamiento del recuento de hipervínculos.
    ErrTotalSheetHyperlinks = errors.New("over maximum limit hyperlinks in a worksheet")
    // ErrInvalidFormula definió el mensaje de error al recibir una fórmula no
    // válida.
    ErrInvalidFormula = errors.New("formula not valid")
    // ErrAddVBAProject definió el mensaje de error al agregar el proyecto VBA
    // en el libro de trabajo.
    ErrAddVBAProject = errors.New("unsupported VBA project extension")
    // ErrMaxRows definió el mensaje de error al recibir un número de fila que
    // excede el límite máximo.
    ErrMaxRows = errors.New("row number exceeds maximum limit")
    // ErrMaxRowHeight definió el mensaje de error al recibir una altura de
    // fila no válida.
    ErrMaxRowHeight = fmt.Errorf("the height of the row must be less than or equal to %d points", MaxRowHeight)
    // ErrImgExt definió el mensaje de error al recibir una extensión de
    // imagen no admitida.
    ErrImgExt = errors.New("unsupported image extension")
    // ErrWorkbookFileFormat definió el mensaje de error al recibir un formato
    // de archivo de libro de trabajo no compatible.
    ErrWorkbookFileFormat = errors.New("unsupported workbook file format")
    // ErrMaxFilePathLength definió el mensaje de error al recibir el
    // desbordamiento de la longitud del nombre de archivo.
    ErrMaxFilePathLength = errors.New("file path length exceeds maximum limit")
    // ErrUnknownEncryptMechanism definió el mensaje de error en un mecanismo
    // de cifrado no compatible.
    ErrUnknownEncryptMechanism = errors.New("unknown encryption mechanism")
    // ErrUnsupportedEncryptMechanism definió el mensaje de error en un
    // mecanismo de cifrado no compatible.
    ErrUnsupportedEncryptMechanism = errors.New("unsupported encryption mechanism")
    // ErrUnsupportedHashAlgorithm definió el mensaje de error en el algoritmo
    // hash no compatible.
    ErrUnsupportedHashAlgorithm = errors.New("unsupported hash algorithm")
    // ErrUnsupportedNumberFormat definió el mensaje de error en la expresión
    // de formato de número no compatible.
    ErrUnsupportedNumberFormat = errors.New("unsupported number format token")
    // ErrPasswordLengthInvalid definió el mensaje de error sobre la longitud
    // de la contraseña no válida.
    ErrPasswordLengthInvalid = errors.New("password length invalid")
    // ErrParameterRequired definió el mensaje de error al recibir el
    // parámetro vacío.
    ErrParameterRequired = errors.New("parameter is required")
    // ErrParameterInvalid definió el mensaje de error al recibir el parámetro
    // no válido.
    ErrParameterInvalid = errors.New("parameter is invalid")
    // ErrDefinedNameScope definió el mensaje de error en el nombre definido
    // no encontrado en el alcance dado.
    ErrDefinedNameScope = errors.New("no defined name on the scope")
    // ErrDefinedNameDuplicate definió el mensaje de error con el mismo nombre
    // que ya existe en el alcance.
    ErrDefinedNameDuplicate = errors.New("the same name already exists on the scope")
    // ErrCustomNumFmt definió el mensaje de error al recibir el formato de
    // número personalizado vacío.
    ErrCustomNumFmt = errors.New("custom number format can not be empty")
    // ErrFontLength definió el mensaje de error sobre la longitud del
    // desbordamiento del nombre de la familia de fuentes.
    ErrFontLength = fmt.Errorf("the length of the font family name must be less than or equal to %d", MaxFontFamilyLength)
    // ErrFontSize definió que el mensaje de error sobre el tamaño de la
    // fuente no es válido.
    ErrFontSize = fmt.Errorf("font size must be between %d and %d points", MinFontSize, MaxFontSize)
    // ErrSheetIdx definió el mensaje de error al recibir el índice de hoja de
    // trabajo no válido.
    ErrSheetIdx = errors.New("invalid worksheet index")
    // ErrUnprotectSheet definió que el mensaje de error en la hoja de trabajo
    // no ha configurado ninguna protección.
    ErrUnprotectSheet = errors.New("worksheet has set no protect")
    // ErrUnprotectSheetPassword definió el mensaje de error al eliminar la
    // protección de hoja con verificación de contraseña fallida.
    ErrUnprotectSheetPassword = errors.New("worksheet protect password not match")
    // ErrGroupSheets definió el mensaje de error en las hojas de grupo.
    ErrGroupSheets = errors.New("group worksheet must contain an active worksheet")
    // ErrDataValidationFormulaLength definió el mensaje de error para recibir
    // una longitud de fórmula de validación de datos que excede el límite.
    ErrDataValidationFormulaLength = fmt.Errorf("data validation must be 0-%d characters", MaxFieldLength)
    // ErrDataValidationRange definió el mensaje de error en un rango decimal
    // establecido que excede el límite.
    ErrDataValidationRange = errors.New("data validation range exceeds limit")
    // ErrCellCharsLength definió el mensaje de error para recibir la longitud
    // de un carácter de celda que excede el límite.
    ErrCellCharsLength = fmt.Errorf("cell value must be 0-%d characters", TotalCellChars)
    // ErrOptionsUnzipSizeLimit definió el mensaje de error para recibir
    // UnzipSizeLimit y UnzipXMLSizeLimit no válidos.
    ErrOptionsUnzipSizeLimit = errors.New("the value of UnzipSizeLimit should be greater than or equal to UnzipXMLSizeLimit")
    // ErrSave definió el mensaje de error para guardar el archivo.
    ErrSave = errors.New("no path defined for file, consider File.WriteTo or File.Write")
    // ErrAttrValBool definió el mensaje de error en el atributo XML de tipo
    // booleano marshal y unmarshal.
    ErrAttrValBool = errors.New("unexpected child of attrValBool")
    // ErrSparklineType definió el mensaje de error al recibir los parámetros
    // de tipo de minigráfico no válidos.
    ErrSparklineType = errors.New("parameter 'Type' must be 'line', 'column' or 'win_loss'")
    // ErrSparklineLocation definió el mensaje de error sobre los parámetros de
    // 'Location' faltantes
    ErrSparklineLocation = errors.New("parameter 'Location' is required")
    // ErrSparklineRange definió el mensaje de error sobre los parámetros de
    // 'Range' del minigráfico que faltan
    ErrSparklineRange = errors.New("parameter 'Range' is required")
    // ErrSparkline definió el mensaje de error al recibir los parámetros de
    // chispa no válidos.
    ErrSparkline = errors.New("must have the same number of 'Location' and 'Range' parameters")
    // ErrSparklineStyle definió el mensaje de error al recibir los parámetros
    // de 'Style' del minigráfico no válidos.
    ErrSparklineStyle = errors.New("parameter 'Style' must between 0-35")
    // ErrWorkbookPassword definió el mensaje de error al recibir la contraseña
    // incorrecta del libro.
    ErrWorkbookPassword = errors.New("the supplied open workbook password is not correct")
)
```

Relación de origen y lista de espacios de nombres, prefijos asociados y esquema en el que se introdujo:

```go
SourceRelationship                      = xml.Attr{Name: xml.Name{Local: "r", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/officeDocument/2006/relationships"}
SourceRelationshipCompatibility         = xml.Attr{Name: xml.Name{Local: "mc", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/markup-compatibility/2006"}
SourceRelationshipChart20070802         = xml.Attr{Name: xml.Name{Local: "c14", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/drawing/2007/8/2/chart"}
SourceRelationshipChart2014             = xml.Attr{Name: xml.Name{Local: "c16", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/drawing/2014/chart"}
SourceRelationshipChart201506           = xml.Attr{Name: xml.Name{Local: "c16r2", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/drawing/2015/06/chart"}
NameSpaceSpreadSheet                    = xml.Attr{Name: xml.Name{Local: "xmlns"}, Value: "http://schemas.openxmlformats.org/spreadsheetml/2006/main"}
NameSpaceSpreadSheetX14                 = xml.Attr{Name: xml.Name{Local: "x14", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/spreadsheetml/2009/9/main"}
NameSpaceDrawingML                      = xml.Attr{Name: xml.Name{Local: "a", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/drawingml/2006/main"}
NameSpaceDrawingMLChart                 = xml.Attr{Name: xml.Name{Local: "c", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/drawingml/2006/chart"}
NameSpaceDrawingMLSpreadSheet           = xml.Attr{Name: xml.Name{Local: "xdr", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing"}
NameSpaceSpreadSheetX15                 = xml.Attr{Name: xml.Name{Local: "x15", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"}
NameSpaceSpreadSheetExcel2006Main       = xml.Attr{Name: xml.Name{Local: "xne", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/excel/2006/main"}
NameSpaceMacExcel2008Main               = xml.Attr{Name: xml.Name{Local: "mx", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/mac/excel/2008/main"}
NameSpaceDocumentPropertiesVariantTypes = xml.Attr{Name: xml.Name{Local: "vt", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes"}
```

IndexedColorMapping es la tabla de asignaciones predeterminadas del valor de color indexado al valor RGB. Tenga en cuenta que 0-7 son redundantes de 8-15 para preservar la compatibilidad con versiones anteriores. Un esquema de indexación heredado para colores que aún se requiere para algunos registros y para la compatibilidad con versiones anteriores de formatos heredados. Este elemento contiene una secuencia de valores de color RGB que corresponden a índices de color (basados en cero). Cuando se utiliza la paleta de colores indexada predeterminada, los valores no se escriben, sino que están implícitos. Cuando la paleta de colores se ha modificado de forma predeterminada, se escribe toda la paleta de colores.

```go
var IndexedColorMapping = []string{
    "000000", "FFFFFF", "FF0000", "00FF00", "0000FF", "FFFF00", "FF00FF", "00FFFF",
    "000000", "FFFFFF", "FF0000", "00FF00", "0000FF", "FFFF00", "FF00FF", "00FFFF",
    "800000", "008000", "000080", "808000", "800080", "008080", "C0C0C0", "808080",
    "9999FF", "993366", "FFFFCC", "CCFFFF", "660066", "FF8080", "0066CC", "CCCCFF",
    "000080", "FF00FF", "FFFF00", "00FFFF", "800080", "800000", "008080", "0000FF",
    "00CCFF", "CCFFFF", "CCFFCC", "FFFF99", "99CCFF", "FF99CC", "CC99FF", "FFCC99",
    "3366FF", "33CCCC", "99CC00", "FFCC00", "FF9900", "FF6600", "666699", "969696",
    "003366", "339966", "003300", "333300", "993300", "993366", "333399", "333333",
    "000000", "FFFFFF",
}
```
