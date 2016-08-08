# ProjetoDistribuicaoProcesso
Distribuição de Processos
Criado no Visual Studio 2015.

Criação do Banco de Dados e Tabela:

CREATE DATABASE Poder Judiciario;
USE [Poder Judiciario]
CREATE TABLE [dbo].[Processo](
	[id] [int] IDENTITY(1,1) NOT NULL,
	[NumeroUnico] [bigint] NULL,
	[Comarca] [varchar](50) NULL,
	[Vara] [varchar](50) NULL,
	[Competencia] [varchar](50) NULL,
	[Descricao] [varchar](500) NULL,
	[Data] [datetime] NULL,
 CONSTRAINT [PK_Processo] PRIMARY KEY CLUSTERED 
(
	[id] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]

Configuração das Conexões no Web Config:

    <add name="Sql" connectionString="Data Source=DESKTOP-VS5IJ5D;Initial Catalog=Poder Judiciario;User ID=sa;Password=1;" providerName="System.Data.SqlClient" />
    <add name="Poder_JudiciarioEntities" connectionString="metadata=res://*/Models.ProcessoModel.csdl|res://*/Models.ProcessoModel.ssdl|res://*/Models.ProcessoModel.msl;provider=System.Data.SqlClient;provider connection string='data source=DESKTOP-VS5IJ5D;initial catalog=&quot;Poder Judiciario&quot;;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework'" providerName="System.Data.EntityClient" />
