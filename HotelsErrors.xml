<?xml version="1.0"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">

	<!-- template for the document root -->
	<xsl:template match="/">

		<html>
			<body>
				<h2>Hotel Directory</h2>

				<table border="1">
					<tr bgcolor="lightgray">
						<th>Name</th>
						<th>Street</th>
						<th>City</th>
						<th>State</th>
						<th>Phone</th>
						<th>Rating</th>
					</tr>

					<!-- iterate over Hotels/Hotel like in notes-->
					<xsl:for-each select="Hotels/Hotel">
						<tr>
							<td>
								<xsl:value-of select="Name"/>
							</td>
							<td>
								<xsl:value-of select="Address/Street"/>
							</td>
							<td>
								<xsl:value-of select="Address/City"/>
							</td>
							<td>
								<xsl:value-of select="Address/State"/>
							</td>

							<!-- print one or more Phone values, comma-separated -->
							<td>
								<xsl:for-each select="Phone">
									<xsl:value-of select="."/>
									<xsl:if test="position()!=last()">, </xsl:if>
								</xsl:for-each>
							</td>

							<!-- attribute value with @ syntax -->
							<td>
								<xsl:value-of select="@Rating"/>
							</td>
						</tr>
					</xsl:for-each>
				</table>

			</body>
		</html>

	</xsl:template>
</xsl:stylesheet>
